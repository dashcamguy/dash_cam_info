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
