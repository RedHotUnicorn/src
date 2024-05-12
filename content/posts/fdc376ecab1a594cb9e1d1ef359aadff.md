---
title: How to automatically update n8n-python
date: 2023-03-15
src_link: https://www.notion.so/How-to-automatically-update-n8n-python-54dbd70514a24a2e8de988b2a581b147
src_date: '2023-03-15 19:41:00'
gold_link: https://blog.davidsha.me/how-to-automatically-update-n8n-python/
gold_link_hash: fdc376ecab1a594cb9e1d1ef359aadff
tags:
- '#host_blog_davidsha_me'
---


[Code](/tag/code/)
How to automatically update n8n-python
======================================


* [![](https://www.gravatar.com/avatar/3425f3d1402b48fb14979cf1b44412be?s=250&r=x&d=mp)](/author/david/)


#### [David Sha](/author/david/)


Apr 14, 2022
• 4 min read

![](/content/images/size/w2000/2022/04/IMG_2587.jpg)


All five tools which we will use in this tutorial.




You followed the instructions from Jan at n8n in [this forum post](https://community.n8n.io/t/running-python-with-n8n/5715/3?u=d4vidsha) and now you have a working `n8n-python` image in Docker on a Linux machine. But after every n8n update, you find that you have to redo these set of steps again. Namely,

1. `docker pull n8nio/n8n`
2. `docker build -t n8n-python .`

But the problem is, you don’t want to do any of this manually. And begin a search to find the best method for automatic updates. Then you come across this page and now you’re invested.

In this tutorial, you will see how to make this all automatic using Watchtower and a bash script.

1. Create `Dockerfile`
2. Create bash script `push-updates.sh`
3. Set up Portainer
4. Set up Watchtower with Portainer
5. Set up n8n with Portainer

Firstly, let us navigate to the directory that we want the script to run in. Any directory of your choosing works, as long as it makes sense to you.


```
cd ~/docker/n8n

```
### 1. Create `Dockerfile`

Start by creating a `Dockerfile`.


```
nano Dockerfile

```
In your `Dockerfile`, add the following lines. Line 3 installs the [requests](https://docs.python-requests.org/en/latest/) library. You can however add more Python libraries here similarly. Line 4 upgrades pip but it is not necessary.


```
FROM n8nio/n8n
RUN apk add --update python3 py3-pip

# installs requests library
RUN python3 -m pip install requests

# upgrades pip (not necessary)
RUN python3 -m pip install --upgrade pip

```
To exit nano `ctrl + x` then `Y`.

### 2. Create bash script `push-updates.sh`

In the same directory,


```
nano push-updates.sh

```
In `push-updates.sh`, add the following lines.


```
#!/bin/bash
username="pixelcoin"                 # docker username
image_name="n8n-python"              # docker image name

docker pull n8nio/n8n
docker build -t $username/$image_name .
docker push $username/$image_name    # you may need to set up docker first 
                                     # with `docker login`.

```
There are three commands in here. Firstly, it pulls the latest image of `n8nio/n8n` from Docker’s repository, then builds our `pixelcoin/n8n-python` image, then pushes the new image to Docker’s repository under our username `pixelcoin`.

Please note that you must be logged in to push to Docker’s repository. In the terminal, run `docker login` and enter your credentials to log in. The username you use will be the same username that gets placed in the `push-updates.sh` file.

Mark `push-updates.sh` as executable by doing the following command:


```
chmod +x push-updates.sh
```
Then set up a cronjob to run this script every day. Of course, you can change the frequency to your needs. In your terminal, type in the following to set up a new scheduled run of your script


```
crontab -e
```
At the end of the file, add


```
0 5 * * * /path/to/push-updates.sh
```
which will run everyday at 5am. Note that you should change `/path/to` to the path where `push-updates.sh` is stored.

### 3. Set up Portainer

We set up Portainer so that we can manage our Docker containers easier. Portainer itself is a docker container. So in your terminal you can run the following command.


```
docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest

```
Now that our container is set up, head over to Portainer in your browser. You will be greeted with a login screen to set up your admin account.

### 4. Set up Watchtower with Portainer

After logging into Portainer, navigate to the following.

![](https://blog.davidsha.me/content/images/2022/04/Markup-2022-04-14-at-17.55.26.png)Under “Name”, call stack “watchtower”.

![](https://blog.davidsha.me/content/images/2022/04/Untitled.png)In the web editor, add the following.


```
version: '2.1'
services:
    watchtower:
        image: containrrr/watchtower:latest
        container_name: watchtower
        volumes:
            - /var/run/docker.sock:/var/run/docker.sock
            - /home/pi/.docker/config.json:/config.json
        environment:
            - WATCHTOWER_CLEANUP=true
            - WATCHTOWER_SCHEDULE= 0 0 04 ? * FRI    # At 04:00 AM, only on Friday
            #- WATCHTOWER_NOTIFICATIONS=email
            #- [[email protected]](/cdn-cgi/l/email-protection)
            #- [[email protected]](/cdn-cgi/l/email-protection)
            #- WATCHTOWER_NOTIFICATION_EMAIL_SERVER=smtp.gmail.com
            #- WATCHTOWER_NOTIFICATION_EMAIL_SERVER_PASSWORD=foo
            #- WATCHTOWER_NOTIFICATION_EMAIL_SUBJECTTAG=Watchtower Alert - Container Updates
            #- [[email protected]](/cdn-cgi/l/email-protection)
            #- WATCHTOWER_NOTIFICATION_EMAIL_SERVER_PORT=465
        restart: always

```
Then at the bottom of the page, “Deploy the stack”.

This `docker-compose.yml` file which you added via the web editor, will update all docker containers at 4am on Friday every week. You can also receive notifications via email if you know how. This is commented out in the above file.

### 5. Set up n8n with Portainer

Now do the same thing but for n8n. In the web editor, you will add this instead.


```
version: "2"
services:
  n8n:
    image: index.docker.io/pixelcoin/n8n-python:latest
    container_name: n8n
    volumes:
      - /PATH/TO/n8n/.n8n:/home/node/.n8n
      - /PATH/TO/n8n/n8n-files:/files
    ports:
      - 5678:5678
    restart: always
    environment:
      - TZ=Australia/Sydney
      - GENERIC_TIMEZONE=Australia/Sydney

```
Take particular note of the image we are pulling. It must be prefixed by `index.docker.io/` for it to be recognised properly by Watchtower. Also pay attention to the `/PATH/TO` in volumes section. These will need to be changed to the path which contain your `.n8n` directory and your `n8n-files` directory.

### That’s it!