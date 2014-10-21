AirPlayMe
=========

I am trying to stream any video file to my Apple TV step by step

Resources
=========

1. Unofficial AirPlay Protocol Specification - http://nto.github.io/AirPlay.html
2. Libavformat Documentation - https://www.ffmpeg.org/libavformat.html

Discovering
=========

AppleTV supports RAOP (Remote Audio Output Protocol) and can be discovered:
```
> dns-sd -B _raop._tcp
Browsing for _raop._tcp
DATE: ---Tue 21 Oct 2014---
18:50:35.786  ...STARTING...
Timestamp     A/R    Flags  if Domain               Service Type         Instance Name
18:50:35.787  Add        2   4 local.               _raop._tcp.          B0349531A808@Apple TV (Гостиная)
```

AppleTV supports AirPlay protocol and can be discovered:
```
> dns-sd -B _airplay._tcp
Browsing for _airplay._tcp
DATE: ---Tue 21 Oct 2014---
18:50:04.576  ...STARTING...
Timestamp     A/R    Flags  if Domain               Service Type         Instance Name
18:50:04.576  Add        2   4 local.               _airplay._tcp.       Apple TV (Гостиная)
```

Getting information about device:
```
> dns-sd -L "Apple TV (Гостиная)" _airplay._tcp
Lookup Apple TV (Гостиная)._airplay._tcp.local
DATE: ---Tue 21 Oct 2014---
18:48:50.316  ...STARTING...
18:48:50.317  Apple TV\032(Гостиная)._airplay._tcp.local. can be reached at AppleTV-Gostinaa.local.:7000 (interface 4) Flags: 2
 deviceid=B0:34:95:31:A8:08 features=0x5A7FFFF7,0x1E flags=0x44 model=AppleTV3,2 pk=4dd33694cf9f462d7dd04c47806ab28753571b393259733ec17b122cfe030771 srcvers=210.98 vv=2
```
