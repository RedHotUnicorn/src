---
title: "GitHub - ArthurFDLR/whisper-youtube: \U0001F509 Youtube Videos Transcription
  with OpenAI's Whisper"
date: 2023-11-05
src_link: https://www.notion.so/ArthurFDLR-whisper-youtube-Youtube-Videos-Transcription-with-OpenAI-s-Whisper-61bd860e22fd40509b6a2f69b64197c1
src_date: '2023-11-05 21:07:00'
gold_link: https://github.com/ArthurFDLR/whisper-youtube
gold_link_hash: 6aa612cdcdbd5cdd8d45f83d305b7a8c
tags:
- '#host_github_com'
---

**Youtube Videos Transcription with OpenAI's Whisper**
======================================================


[![](https://camo.githubusercontent.com/f500ee647e55bda771b595adab71fb14e6f3e32f3dbe6804685d78efc3e5e70d/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f6c6162656c3d266d6573736167653d426c6f67253230706f737426636f6c6f723d626c7565267374796c653d666f722d7468652d6261646765266c6f676f3d6f70656e6169266c696e6b3d68747470733a2f2f6f70656e61692e636f6d2f626c6f672f77686973706572)](https://openai.com/blog/whisper)
[![](https://camo.githubusercontent.com/0e62ed687e8bdce11d348e0f7974e14895cca8dfe4ce6ea2822477983a25bac8/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f6c6162656c3d266d6573736167653d4e6f7465626f6f6b26636f6c6f723d626c7565267374796c653d666f722d7468652d6261646765266c6f676f3d676f6f676c65636f6c6162266c696e6b3d68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6769746875622f41727468757246444c522f776869737065722d796f75747562652f626c6f622f6d61696e2f776869737065725f796f75747562652e6970796e62)](https://colab.research.google.com/github/ArthurFDLR/whisper-youtube/blob/main/whisper_youtube.ipynb)
[![](https://camo.githubusercontent.com/74bcdd0f6c44c734909b29e36bb15935b755ac320741de39feb2ad0ad3813219/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f6c6162656c3d266d6573736167653d5265706f7369746f727926636f6c6f723d626c7565267374796c653d666f722d7468652d6261646765266c6f676f3d676974687562266c696e6b3d68747470733a2f2f6769746875622e636f6d2f6f70656e61692f77686973706572)](https://github.com/openai/whisper)
[![](https://camo.githubusercontent.com/496b2869fc39ac80f8cf5579e6722c820f7c0a3068eb8e53cacaed1d4e5b016b/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f6c6162656c3d266d6573736167653d506170657226636f6c6f723d626c7565267374796c653d666f722d7468652d6261646765266c696e6b3d68747470733a2f2f63646e2e6f70656e61692e636f6d2f7061706572732f776869737065722e706466)](https://cdn.openai.com/papers/whisper.pdf)
[![](https://camo.githubusercontent.com/624b07c3d7132e47d850cde4927d971e3861ef4cc832be92dbb898ca57ccdea6/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f6c6162656c3d266d6573736167653d4d6f64656c2532306361726426636f6c6f723d626c7565267374796c653d666f722d7468652d6261646765266c696e6b3d68747470733a2f2f6769746875622e636f6d2f6f70656e61692f776869737065722f626c6f622f6d61696e2f6d6f64656c2d636172642e6d64)](https://github.com/openai/whisper/blob/main/model-card.md)


Whisper is a general-purpose speech recognition model. It is trained on a large dataset of diverse audio and is also a multi-task model that can perform multilingual speech recognition as well as speech translation and language identification.


This notebook will guide you through the transcription of a Youtube video using Whisper. You'll be able to explore most inference parameters or use the Notebook as-is to store the transcript and the audio of the video in your Google Drive.


**Check GPU type** 🕵️
=====================


The type of GPU you get assigned in your Colab session defined the speed at which the video will be transcribed.
The higher the number of floating point operations per second (FLOPS), the faster the transcription.
But even the least powerful GPU available in Colab is able to run any Whisper model.
Make sure you've selected `GPU` as hardware accelerator for the Notebook (Runtime → Change runtime type → Hardware accelerator).




| GPU | GPU RAM | FP32 teraFLOPS | Availability |
| --- | --- | --- | --- |
| T4 | 16 GB | 8.1 | Free |
| P100 | 16 GB | 10.6 | Colab Pro |
| V100 | 16 GB | 15.7 | Colab Pro (Rare) |




---


**Factory reset your Notebook's runtime if you want to get assigned a new GPU.**



```
    GPU 0: Tesla T4 (UUID: GPU-9ba4ce04-e020-44f9-8fc3-337ba5bb5496)
    Sun Oct  2 16:49:51 2022       
    +-----------------------------------------------------------------------------+
    | NVIDIA-SMI 460.32.03    Driver Version: 460.32.03    CUDA Version: 11.2     |
    |-------------------------------+----------------------+----------------------+
    | GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
    | Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
    |                               |                      |               MIG M. |
    |===============================+======================+======================|
    |   0  Tesla T4            Off  | 00000000:00:04.0 Off |                    0 |
    | N/A   36C    P8     9W /  70W |      0MiB / 15109MiB |      0%      Default |
    |                               |                      |                  N/A |
    +-------------------------------+----------------------+----------------------+
                                                                                   
    +-----------------------------------------------------------------------------+
    | Processes:                                                                  |
    |  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
    |        ID   ID                                                   Usage      |
    |=============================================================================|
    |  No running processes found                                                 |
    +-----------------------------------------------------------------------------+

```

**Install libraries** 🏗️
========================


This cell will take a little while to download several libraries, including Whisper.




---



```
    Looking in indexes: https://pypi.org/simple, https://us-python.pkg.dev/colab-wheels/public/simple/
    Collecting git+https://github.com/openai/whisper.git
      Cloning https://github.com/openai/whisper.git to /tmp/pip-req-build-c3voj3wy
      Running command git clone -q https://github.com/openai/whisper.git /tmp/pip-req-build-c3voj3wy
    Requirement already satisfied: numpy in /usr/local/lib/python3.7/dist-packages (from whisper==1.0) (1.21.6)
    Requirement already satisfied: torch in /usr/local/lib/python3.7/dist-packages (from whisper==1.0) (1.12.1+cu113)
    Requirement already satisfied: tqdm in /usr/local/lib/python3.7/dist-packages (from whisper==1.0) (4.64.1)
    Requirement already satisfied: more-itertools in /usr/local/lib/python3.7/dist-packages (from whisper==1.0) (8.14.0)
    Requirement already satisfied: transformers>=4.19.0 in /usr/local/lib/python3.7/dist-packages (from whisper==1.0) (4.22.2)
    Requirement already satisfied: ffmpeg-python==0.2.0 in /usr/local/lib/python3.7/dist-packages (from whisper==1.0) (0.2.0)
    Requirement already satisfied: future in /usr/local/lib/python3.7/dist-packages (from ffmpeg-python==0.2.0->whisper==1.0) (0.16.0)
    Requirement already satisfied: huggingface-hub<1.0,>=0.9.0 in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (0.10.0)
    Requirement already satisfied: pyyaml>=5.1 in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (6.0)
    Requirement already satisfied: importlib-metadata in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (4.12.0)
    Requirement already satisfied: tokenizers!=0.11.3,<0.13,>=0.11.1 in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (0.12.1)
    Requirement already satisfied: requests in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (2.23.0)
    Requirement already satisfied: regex!=2019.12.17 in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (2022.6.2)
    Requirement already satisfied: packaging>=20.0 in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (21.3)
    Requirement already satisfied: filelock in /usr/local/lib/python3.7/dist-packages (from transformers>=4.19.0->whisper==1.0) (3.8.0)
    Requirement already satisfied: typing-extensions>=3.7.4.3 in /usr/local/lib/python3.7/dist-packages (from huggingface-hub<1.0,>=0.9.0->transformers>=4.19.0->whisper==1.0) (4.1.1)
    Requirement already satisfied: pyparsing!=3.0.5,>=2.0.2 in /usr/local/lib/python3.7/dist-packages (from packaging>=20.0->transformers>=4.19.0->whisper==1.0) (3.0.9)
    Requirement already satisfied: zipp>=0.5 in /usr/local/lib/python3.7/dist-packages (from importlib-metadata->transformers>=4.19.0->whisper==1.0) (3.8.1)
    Requirement already satisfied: certifi>=2017.4.17 in /usr/local/lib/python3.7/dist-packages (from requests->transformers>=4.19.0->whisper==1.0) (2022.6.15)
    Requirement already satisfied: idna<3,>=2.5 in /usr/local/lib/python3.7/dist-packages (from requests->transformers>=4.19.0->whisper==1.0) (2.10)
    Requirement already satisfied: chardet<4,>=3.0.2 in /usr/local/lib/python3.7/dist-packages (from requests->transformers>=4.19.0->whisper==1.0) (3.0.4)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in /usr/local/lib/python3.7/dist-packages (from requests->transformers>=4.19.0->whisper==1.0) (1.24.3)
    Looking in indexes: https://pypi.org/simple, https://us-python.pkg.dev/colab-wheels/public/simple/
    Requirement already satisfied: pytube in /usr/local/lib/python3.7/dist-packages (12.1.0)


    Using device: cuda:0

```

**Optional:** Save images in Google Drive 💾
===========================================


Enter a Google Drive path and run this cell if you want to store the results inside Google Drive.




---


`drive_path = "Colab Notebooks/Whisper Youtube"`




---


**Run this cell again if you change your Google Drive path.**


**Model selection** 🧠
=====================


As of the first public release, there are 4 pre-trained options to play with:




| Size | Parameters | English-only model | Multilingual model | Required VRAM | Relative speed |
| --- | --- | --- | --- | --- | --- |
| tiny | 39 M | `tiny.en` | `tiny` | ~1 GB | ~32x |
| base | 74 M | `base.en` | `base` | ~1 GB | ~16x |
| small | 244 M | `small.en` | `small` | ~2 GB | ~6x |
| medium | 769 M | `medium.en` | `medium` | ~5 GB | ~2x |
| large | 1550 M | N/A | `large` | ~10 GB | 1x |




---


`Model = 'large'`




---


**Run this cell again if you change the model.**



```
    100%|█████████████████████████████████████| 2.87G/2.87G [01:14<00:00, 41.5MiB/s]

```

**large model is selected.**


**Video selection** 📺
=====================


Enter the URL of the Youtube video you want to transcribe, whether you want to save the audio file in your Google Drive, and run the cell.




---


`URL = "https://youtu.be/dQw4w9WgXcQ"`


`store_audio = True`




---


**Run this cell again if you change the video.**


**Run the model** 🚀
===================


Run this cell to execute the transcription of the video. This can take a while and is very much based on the length of the video and the number of parameters of the model selected above.




---


`Language = "English"`


`Output_type = '.vtt'`




---



```
    [00:00.000 --> 00:22.000]  We're no strangers to love.
    [00:22.000 --> 00:27.000]  You know the rules, and so do I.
    [00:27.000 --> 00:31.000]  Our full commitments while I'm thinking of.
    [00:31.000 --> 00:35.000]  You wouldn't get this from any other guy.
    [00:35.000 --> 00:40.000]  I just wanna tell you how I'm feeling.
    [00:40.000 --> 00:43.000]  Gotta make you understand.
    [00:43.000 --> 00:45.000]  Never gonna give you up.
    [00:45.000 --> 00:47.000]  Never gonna let you down.
    [00:47.000 --> 00:51.000]  Never gonna run around and desert you.
    [00:51.000 --> 00:53.000]  Never gonna make you cry.
    [00:53.000 --> 00:55.000]  Never gonna say goodbye.
    [00:55.000 --> 01:00.000]  Never gonna tell a lie and hurt you.
    [01:00.000 --> 01:04.000]  We've known each other for so long.
    [01:04.000 --> 01:09.000]  Your heart's been aching, but you're too shy to say it.
    [01:09.000 --> 01:13.000]  Inside we both know what's been going on.
    [01:13.000 --> 01:17.000]  We know the game and we're gonna play it.
    [01:17.000 --> 01:22.000]  And if you ask me how I'm feeling.
    [01:22.000 --> 01:25.000]  Don't tell me you're too blind to see.
    [01:25.000 --> 01:27.000]  Never gonna give you up.
    [01:27.000 --> 01:29.000]  Never gonna let you down.
    [01:29.000 --> 01:33.000]  Never gonna run around and desert you.
    [01:33.000 --> 01:35.000]  Never gonna make you cry.
    [01:35.000 --> 01:38.000]  Never gonna say goodbye.
    [01:38.000 --> 01:41.000]  Never gonna tell a lie and hurt you.
    [01:41.000 --> 01:43.000]  Never gonna give you up.
    [01:43.000 --> 01:46.000]  Never gonna let you down.
    [01:46.000 --> 01:50.000]  Never gonna run around and desert you.
    [01:50.000 --> 01:59.000]  Never gonna make you cry, never gonna say goodbye, never gonna tell a lie and hurt you
    [01:59.000 --> 02:07.000]  Give you love, give you love
    [02:07.000 --> 02:16.000]  Never gonna give, never gonna give, give you love
    [02:16.000 --> 02:25.000]  We've known each other for so long, your heart's been aching but you're too shy to say it
    [02:25.000 --> 02:33.000]  Inside we both know what's been going on, we know the game and we're gonna play it
    [02:33.000 --> 02:41.000]  I just wanna tell you how I'm feeling, gotta make you understand
    [02:41.000 --> 02:49.000]  Never gonna give you up, never gonna let you down, never gonna run around and desert you
    [02:49.000 --> 02:57.000]  Never gonna make you cry, never gonna say goodbye, never gonna tell a lie and hurt you
    [02:57.000 --> 03:06.000]  Never gonna give you up, never gonna let you down, never gonna run around and desert you
    [03:06.000 --> 03:14.500]  Never gonna make you cry, never gonna say goodbye, never gonna tell a lie, and hurt you.
    [03:14.500 --> 03:23.000]  Never gonna give you up, never gonna let you down, never gonna run around and desert you.
    [03:23.000 --> 03:27.500]  We're gonna make you cry, we're gonna say goodbye,
    [03:27.500 --> 03:53.400]  we're gonna say goodbye.

```

**Transcript file created: /content/drive/My Drive/Colab Notebooks/Whisper Youtube/dQw4w9WgXcQ.vtt**