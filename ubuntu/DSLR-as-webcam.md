# [DSLR as a webcam](https://medium.com/nerdery/dslr-webcam-setup-for-linux-9b6d1b79ae22)

```shell
sudo apt-get install gphoto2 v4l2loopback-utils v4l2loopback-dkms ffmpeg
```
## start-video.sh

```shell
#!/bin/bash

sudo modprobe v4l2loopback exclusive_caps=1 max_buffers=2
gphoto2 --stdout --capture-movie | ffmpeg -i - -vcodec rawvideo -pix_fmt yuv420p -threads 0 -f v4l2 /dev/video0
```

## VLC

`CTRL + C` -> `/dev/video0`

## Done

Now You can start the meeting (tested on Zoom.us).
