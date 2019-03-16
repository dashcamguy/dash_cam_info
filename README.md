# dash_cam_info
Educational materials related to dashboard cameras

## Yi Mini Dash Cam

### RTSP stream

It's at rtsp://192.168.1.254/livestream/12

Looks like it's video-only

Device crashes and resets after a few seconds of streaming when using VLC

Stream doesn't open up at all on TinyCam

Port scanning makes the device reset.

Open ports:

* 21 (ftp)

* 80 (http)

* 554 (rtsp)

* 2223 (rockwell-csp2 ???)

* 2226 (di-drm ???)

* 3333 (dec-notes ???)

* 5001 (commplex-link ???)

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
