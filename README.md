~~~
$ gst-launch-1.0 souphttpsrc location="http://192.168.0.14:8080/videofeed" is_live=true ! jpegdec ! autovideosink
$ gst-launch-1.0 souphttpsrc location="http://192.168.0.14:8080/videofeed" is_live=true ! jpegdec ! videoconvert ! v4l2sink device=/dev/video1

$ pactl load-module module-jack-sink
~~~
