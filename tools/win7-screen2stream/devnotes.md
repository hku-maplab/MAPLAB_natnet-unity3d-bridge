
Screen capture on windows:
* Gstreamer 1.0 (!)
* screen-capture-recorder http://gstreamer.freedesktop.org/data/pkg/windows/1.0.10/

Send stream:

  @echo off
  
  set /p HOST="Enter host or ipaddress: "
  
  echo "Sending screen to %HOST%"
  
  gst-launch-1.0.exe gdiscreencapsrc ! videoconvert ! video/x-raw,format=I420 ! jpegenc ! rtpjpegpay ! udpsink host=%HOST% port=5000


Playback on android:
* GoodPlayer https://play.google.com/store/apps/details?id=com.hustmobile.goodplayer&hl=en
