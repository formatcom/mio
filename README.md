### CAPTURE VIDEO DEVICE
~~~
$ v4l2-ctl --list-devices
~~~

### SOUND DEVICE
~~~
$ aplay -l
~~~

### CONF SOUND
~~~
$ alsamixer
~~~

### IP WEBCAM
~~~
$ gst-launch-1.0 souphttpsrc location="http://ip:port/videofeed" is_live=true ! jpegdec ! autovideosink
$ gst-launch-1.0 souphttpsrc location="http://ip:port/videofeed" is_live=true ! jpegdec ! videoconvert ! v4l2sink device=/dev/video1
~~~

### SOUND
~~~
$ pactl load-module module-jack-sink
$ pactl load-module module-jack-source
~~~

### MIC TO SPEAKERS
~~~
# pactl load-module module-loopback latency_msec=1
~~~

### ALSA ADD QJACKCTL
~~~
$ cat /proc/asound/cards
$ alsa_in  -d hw:0
$ alsa_out -d hw:0
~~~
