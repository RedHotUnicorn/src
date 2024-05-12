---
title: 'GitHub - aschmelyun/subvert: Generate subtitles, summaries, and chapters from
  videos in seconds'
date: 2023-03-30
src_link: https://www.notion.so/GitHub-aschmelyun-subvert-Generate-subtitles-summaries-and-chapters-from-videos-in-seconds-932da5cdb86b4c0d8ba6a1d48726a466
src_date: '2023-03-30 18:04:00'
gold_link: https://github.com/aschmelyun/subvert
gold_link_hash: dccee93de715524fa8dceffd276eff39
tags:
- '#host_github_com'
---

Subvert
=======


[![](https://camo.githubusercontent.com/3d463223608fa24db19a98ec20a16684a72760e11e220959a1ff490361998366/68747470733a2f2f696d672e736869656c64732e696f2f646f636b65722f762f617363686d656c79756e2f737562766572743f7374796c653d666c61742d737175617265)](https://camo.githubusercontent.com/3d463223608fa24db19a98ec20a16684a72760e11e220959a1ff490361998366/68747470733a2f2f696d672e736869656c64732e696f2f646f636b65722f762f617363686d656c79756e2f737562766572743f7374796c653d666c61742d737175617265)
[![](https://camo.githubusercontent.com/8d9a834a3053e8aa5f2813b4ce264e8e39d241787aed5e422ca6ffc386238402/68747470733a2f2f696d672e736869656c64732e696f2f646f636b65722f70756c6c732f617363686d656c79756e2f737562766572743f6c6162656c3d70756c6c73267374796c653d666c61742d737175617265)](https://camo.githubusercontent.com/8d9a834a3053e8aa5f2813b4ce264e8e39d241787aed5e422ca6ffc386238402/68747470733a2f2f696d672e736869656c64732e696f2f646f636b65722f70756c6c732f617363686d656c79756e2f737562766572743f6c6162656c3d70756c6c73267374796c653d666c61742d737175617265)


Generate subtitles, chapters, and summaries of videos in seconds with the help of OpenAI.


🚧 This is very much a work-in-progress, please [create issues](https://github.com/aschmelyun/subvert/issues/new) for bugs if they appear 🚧


[![](/aschmelyun/subvert/raw/main/media/subvert-demo.gif)](/aschmelyun/subvert/blob/main/media/subvert-demo.gif)


Getting started
---------------


You'll need:


* [Docker installed](https://docs.docker.com/get-docker/) on your local machine
* An [OpenAI API key](https://platform.openai.com/account/api-keys)


Subvert is self-contained in a single Docker image and can be started with a one-line command:



```
docker run -it -p 80:8080 -e OPENAI_API_KEY=sk-123abc aschmelyun/subvert

```

This will boot up a server running the application and make it available to your machine at [http://localhost](http://localhost).


How it works
------------


After selecting a video file to process, you have the option of choosing whether you also want to generate chapters and a summary.


Your video is sent to an API where the audio is extracted from it using FFMpeg, and then sent to **OpenAI's Whisper model** for transcription into the common vtt format.


If you chose to select chapters or a summary, that transcript is then sent to a **ChatGPT model** for processing into concise chapters of the length you wanted, and a brief summary that would fit in something like a YouTube description.


Configuration
-------------


You can adjust a few parameters in the container by passing in [environment variables](https://docs.docker.com/engine/reference/commandline/run/#env) with your command using additional `-e` flags. Here are the current ones you can add:


* `OPENAI_API_KEY` **(required)** - Sets the key responsible for communication with OpenAI's APIs. No default.
* `UPLOAD_MAX_FILESIZE` - Changes PHP's UPLOAD\_MAX\_FILESIZE setting. Default: `256M`
* `MEMORY_LIMIT` - Changes PHP's MEMORY\_LIMIT setting. Default: `512M`


Starting from source
--------------------


Alternative, if you have **PHP 8.1+** and **npm** installed on your local machine, you can boot the application up directly from the source code instead.


First, check out this repo to your desired location. Then, navigate to the `src` directory and run:



```
./startup.sh

```

Alternatively, you can run the commands inside of the `startup.sh` script individually for the same result.


Deploying
---------


Because this project is contained in a single Dockerfile, it can be deployed immediately to any server provisioned with Docker. Alternatively, the Subvert Docker image can be ran on cloud instances via AWS, Azure, GCP, Fly.io, etc.



> Note: This image currently only exposes the insecure :80 http port.


License
-------


The MIT License (MIT). Please see [License File](/aschmelyun/subvert/blob/main/LICENSE.md)