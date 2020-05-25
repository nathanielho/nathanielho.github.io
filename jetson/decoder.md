_18th May 2020_

Packing a GPU with half a Teraflop, the [Nvidia Jetson Nano](https://developer.nvidia.com/embedded/jetson-nano-developer-kit) is well suited to some light video processing. It probably can't do heavy encoding tasks as its IO bus speeds are not that great to bring in raw video (the Jetson Xavier is better for that), adding to the fact the audio encoding is done on the CPU (which is not the strongest point of the Jetson Nano). However decoding is a different matter, the output interface to the HDMI/DisplayPort should be rather good and allow for smooth video and decoding audio on CPU is less demanding.

I am looking at projects to use it as device for receiving an internet protected video stream using an ARQ protocol such as RIST/SRT/Zixi but first we need to get the decoder operational.

The Ubuntu Linux that Nvidia packages in the [Jetpack image](https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit#write) now comes with GStreamer already installed. To save you a bit of time from looking into the [manual](https://developer.nvidia.com/embedded/dlc/l4t-accelerated-gstreamer-guide-32-1), you can play a file and output it on X11 by using this command:
```
gst-launch-1.0 filesrc location=<filename.mp4> ! \ 
qtdemux name=demux demux.video_0 ! queue ! h264parse ! omxh264dec ! \
nveglglessink -e
```



