### CAPTURE DEVICE
~~~
$ v4l2-ctl --list-devices
~~~

### IP WEBCAM
~~~
$ gst-launch-1.0 souphttpsrc location="http://ip:port/videofeed" is_live=true ! jpegdec ! autovideosink
$ gst-launch-1.0 souphttpsrc location="http://ip:port/videofeed" is_live=true ! jpegdec ! videoconvert ! v4l2sink device=/dev/video1
~~~

### SOUND
~~~
$ pactl load-module module-jack-sink
~~~

### MIC TO SPEAKERS
~~~
# pactl load-module module-loopback latency_msec=1
~~~
