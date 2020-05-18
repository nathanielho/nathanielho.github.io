With a GPU with half a Teraflop, the Jetson Nano is well suited to some video processing. Although its IO bus speeds are not that great, I think it would be quite limited in bringing video in, however the output to the HDMI/DisplayPort should be rather good.

I am looking at projects to use it as device for receiving an internet protected video stream using RIST/SRT/Zixi. But first we need to get the decoder side operational.

The Jetson Nano image comes with gstreamer already installed. To save you a bit of time from the [manual](https://developer.nvidia.com/embedded/dlc/l4t-accelerated-gstreamer-guide-32-1), you can play a file and output it on X11 by using this command:
```
gst-launch-1.0 filesrc location=<filename.mp4> ! \ 
qtdemux name=demux demux.video_0 ! queue ! h264parse ! omxh264dec ! \
nveglglessink -e
```