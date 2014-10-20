AirPlayMe
=========

I am trying to stream any video file to my Apple TV step by step

Resources
=========

1. Unofficial AirPlay Protocol Specification - http://nto.github.io/AirPlay.html
2. Libavformat Documentation - https://www.ffmpeg.org/libavformat.html

Discovering
=========

This can discover all AppleTV's in local network:
```
dns-sd -B _raop._tcp
```
