---
published: true
layout: post
title: Youtube Downloader!
categories: Linux
tags: [command line],[linux application]
---

Youtube-dl is an open source program written in Python for the command line but it does more than just download audio and video from youtube.

### Installing Youtube-dl

Using Curl

$ sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl

Using wget

$ sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl

$ sudo chmod a+rx /usr/local/bin/youtube-dl

After installing it remember to update it

$ sudo youtube-dl -U

### Using Youtube-dl

#### 1. To download a video

$ youtube-dl https://www.youtube.com/watch?v=yJg-Y5byMMw

#### 2. To download a video and save with a specific name

$ youtube-dl -o 'Warriyo - Mortals (feat. Laura Brehm)[NCS]' https://www.youtube.com/watch?v=yJg-Y5byMMw

#### 3. To download a video and save in a specific location

$ youtube-dl -o '~/Downloads/Warriyo - Mortals (feat. Laura Brehm)[NCS]' https://www.youtube.com/watch?v=yJg-Y5byMMw

#### 4. To download multiple videos

$ youtube-dl <url1> <url2>
  
#### 5. To download multiple videos by passing a text file with multiple links

$ youtube-dl -a url.txt

#### 6. To list all available formats of video

$ youtube-dl --list-formats https://www.youtube.com/watch?v=yJg-Y5byMMw

$ youtube-dl -F https://www.youtube.com/watch?v=yJg-Y5byMMw

#### 7. To download videos in specific quality and format. 

Note that the following options may be available but not always.

|Option|Remarks|
|:---:|:---:|
|best|select the best quality format for the given file with video and audio|
|worst|select the worst quality format of the given file with video and audio|
|bestvideo|select the best quality video-only format|
|worstvideo|select the worst quality video-only format|
|bestaudio|select the best quality audio only-format|
|worstaudio|select the worst quality audio only-format|

Example:

$ youtube-dl -f bestaudio https://www.youtube.com/watch?v=yJg-Y5byMMw

You can also combine formats and merge them with ffmpeg (remember to have ffmpeg installed).

$ youtube-dl -f bestvideo+bestaudio https://www.youtube.com/watch?v=yJg-Y5byMMw

You may also specify multiple format codes in any preferred order from the listed format you have listed in 6 above.

$ youtube-dl -f 22/17/18 <playlist_url>

#### 8. To download videos by specific format

$ youtube-dl --format mp4 https://www.youtube.com/watch?v=yJg-Y5byMMw

#### 9. To set size limit for videos

$ youtube-dl --min-filesize 100M <playlist_url>

$ youtube-dl --max-filesize 100M <playlist_url>

$ youtube-dl -f 'best[filesize<100M]' <playlist_url>

#### 10. To download the 10th file from a playlist

$ youtube-dl --playlist-items 10 <playlist_url>

#### 11. To download multiple random files

$ youtube-dl --playlist-items 2,3,7,10 <playlist_url>

#### 12. To download a video playlist starting from a certain video

$ youtube-dl --playlist-start 10 <playlist_url>

#### 13. To download only the files starting from 2nd to 5th in a playlist

$ youtube-dl --playlist-start 2 --playlist-end 5 <playlist_url>

#### 14. To download audio only from a video (note that the default is in ogg format)

$ youtube-dl -x https://www.youtube.com/watch?v=yJg-Y5byMMw

#### 15. To download audio only in mp3 format

$ youtube-dl -x --audio-format mp3 https://www.youtube.com/watch?v=yJg-Y5byMMw
