# dash_cam_info
Educational materials related to dashboard cameras. The information in this repository is for educational purposes only.

## Yi Mini Dash Cam

### Device firmware version

This info is valid as of Firmware 1.01.19b_US

If you've got a different firmware, there may be things changed in that firmware you've got

### Raspberry Pi NodeJS HTTP app for Yi Dash Cam recording

This repo contains what looks like a great app that interacts with the Yi Dash Cam: https://github.com/tjwoon/sentinel

Plus description of how it works, via the HTTP commands

### RTSP stream

It's at rtsp://192.168.1.254/livestream/12

Looks like it's video-only, using H264 and RTP/AVP

### Commands

Commands to the device seem to follow this format:

http://192.168.1.254/?custom=1&cmd=3034&str=2019-03-16_10:30:26

Responses seem to be in XML

### Software

"jl 0.01 streaming server"

Might be using "lwIP - A Lightweight TCP/IP stack"

HTTP Server appears to be "eCos/1.0"

### Oddities

Device crashes and resets after a few seconds of streaming when using VLC

Stream doesn't open up at all on TinyCam

Works fine using the official Yi Dashcam android app. Commands via HTTP may be necessary to keep the stream open.

Port scanning makes the device reset.

### Open ports

* 21 (ftp)

* 80 (http)

* 554 (rtsp)

* 2223 (rockwell-csp2 ???)

* 2226 (di-drm ???)

* 3333 (dec-notes ???)

* 5001 (commplex-link ???)

### Overview

Fun to play around with, but could be better.

Seems to be pretty heavily focused on getting you to use the Yi Dash Cam app. Gotta use it to set up the camera, turn off the logo, and change the wifi ssid and password.

## Pruveeo F5 Dash Cam

### Streaming video

MJPEG stream at http://192.168.25.1:8080/?action=stream

* Works on TinyCam and VLC
* Just a JPG image stream
* Only about 12 frames per second
* NO AUDIO

### Command port

Command port is 8081

### HTTP Login page
Chinese-only login page at http://192.168.25.1

Translation of the login page:
```
用户登陆 = user login
用户名 = username
密码 = password
[登陆] = Landing
[重買] = rebuy
```

Can login with no username or password. Just click the "Landing" button.

Logs you into a router config app which appears to be made by "South Silicon Valley"

I'm guessing there's a SSV6051Z or SSV6051P chip in this device. Haven't yet opened it up to confirm.

### Overview

Overall, this device seems to be a pretty great deal for $30

Audio streaming via RTSP and a higher frame rate would be significant improvements to this device

8081 appears to be the "Command Port" where you can send the commands to set settings on the device

Can change the wifi SSID and password within the device control menu. Great features!
