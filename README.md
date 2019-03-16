# dash_cam_info
Educational materials related to dashboard cameras

## Yi Mini Dash Cam

Looks like the RTSP stream is at rtsp://192.168.1.254/livestream/12 but I haven't streamed it from there yet.

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

Overall, this device seems to be a pretty great deal for $30
