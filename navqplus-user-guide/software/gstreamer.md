# GStreamer

## Pipeline examples

### Take an image

```
gst-launch-1.0 -v v4l2src num-buffers=1 device=/dev/video3 ! jpegenc ! filesink location=capture.jpeg
```

### Record a video

```
gst-launch-1.0 v4l2src device=/dev/video3 ! imxvideoconvert_g2d ! "video/x-raw, height=640, width=480, framerate=30/1" ! vpuenc_h264 ! avimux ! filesink location='/home/user/video.avi'
```

## Streaming examples:

* On PC: RX Pipeline to receive the stream from the NavQPlus AI/ML companion computer:

`gst-launch-1.0 udpsrc port=50000 ! "application/x-rtp, media=(string)video, clock-rate=(int)90000, encoding-name=(string)H264, payload=(int)96" ! rtph264depay ! decodebin ! queue ! autovideosink`

&#x20;

* On NavQPlus (e.g. from SSH connection):

`gst-launch-1.0 v4l2src io-mode=dmabuf device=/dev/video3 ! "video/x-raw,width=1920,height=1080,framerate=(fraction)30/1" ! vpuenc_h264 ! h264parse ! rtph264pay ! udpsink host=10.0.1.101 port=50000`



{% hint style="success" %}
Note: Modify the host IP address 10.0.1.101 to the one matching your receiving laptop
{% endhint %}

&#x20;

* Video Test Source instead of camera:\
  `gst-launch-1.0 videotestsrc ! "video/x-raw,width=640,height=480,framerate=(fraction)10/1" ! vpuenc_h264 ! h264parse ! rtph264pay ! udpsink host=10.0.1.101 port=50000`



* Camera Tuning:\
  1\) Get the video subdevice using:

&#x20;    `media-ctl -p /dev/media0`

&#x20;    remember the sub-device of the camera ( ov5645tn) in the media video chain, e.g. /dev/v4l-subdev2

\
2\) List the available user and camera controls and try them out (e.g. contrast, saturation, auto white balancing etc.):

&#x20;   `v4l2-ctl -l -d /dev/v4l-subdev2`

&#x20;

* Streaming and Storing to a h264 compressed file simultaneously including text overlays for 30 seconds:

`gst-launch-1.0 v4l2src io-mode=dmabuf device=/dev/video3 num-buffers=900 ! "video/x-raw,width=1920,height=1080,framerate=(fraction)30/1" ! tee name=t ! queue leaky=1 ! textoverlay text="Live" ! vpuenc_h264 ! h264parse ! rtph264pay ! udpsink host=10.0.1.101 port=50000 sync=false t. ! queue ! textoverlay text="recorded" ! vpuenc_h264 ! mpegtsmux ! filesink location=record_$(date +"%Y-%m-%d_%T").mp4`

\
Note: The VPU is encoding two streams in parallel as we have different text overlays on the live stream and the recorded file&#x20;

&#x20;

&#x20;

### Note on hostapd

* To avoid setting up a Wi-Fi router `hostapd` was installed so that the NavQPlus is an access point. Also, a DHCP server was configured. This way I could directly connect to the WiFi network which was spawned by the NavQPlus:
* IP address 10.0.1.101 is coming from the DHCP server on the NavQPlus.

&#x20;\
