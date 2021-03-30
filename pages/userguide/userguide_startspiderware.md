---
title: Starting SpiderWare
keywords: spiderware
sidebar: userguide_sidebar
permalink: userguide_startspiderware.html
folder: userguide
toc: true
---

------

Whether you SpiderWare is installed in a server or in the camera, there is only one way to start SpiderWare.

### Linux

1. Open a terminal

2. Go to the directory to where SpiderWare is installed

3. Run `./spiderware <path to config file> <path to license file>`

   ```
   ./spiderware config/config.json LICENSE
   ```



### Windows

1. Open a terminal

2. Go to the directory to where SpiderWare is installed

3. Run `spiderware.exe <path to config file> <path to license file>`

   ```
   spiderware.exe config/config.json LICENSE
   ```



## Other OS

1. Open a terminal

2. Go to the directory to where SpiderWare is installed

3. Run `./spiderware <path to config file> <path to license file>`

   ```
   ./spiderware config/config.json LICENSE
   ```



**Notes:**

- Using Linux OS: If no config file and/or license file was given, SpiderWare shall look at the current directory and search for config.json and LICENSE file

- A successful startup will show the connected audio and video sources, the EXM server and session where it will connect.



## SpiderWare Startup

```
Reading license from LICENSE
Validating License
Activating SpiderWare 1.0.3...
Initializing signal handlers...
Starting web server...
Web service module started at port 9090.
Starting webrtc module...
Instance ID:
Initializing exchange module client...
Exchange module server: https://exm.evostream.com:5555
[2021-03-30 23:40:51] [connect] Successful connection
[2021-03-30 23:40:52] [connect] WebSocket Connection 149.28.186.33:5555 v-2 "WebSocket++/0.8.2" /socket.io/?EIO=4&transport=websocket&t=1617118850 101
Exchange module connected.
Detecting video and audio sources...
Video sources:
[ "Lenovo EasyCamera", "Wirecast Virtual Camera" ]

Audio sources:
[ "Microphone (Realtek High Definition Audio)" ]

Webrtc module started. Ready to accept connections.
SpiderWare activated.
```

**Note:**  If a license file is not found, the application will generate an Instance ID. The instance ID is unchanging not unless the init file is deleted.



## Binded License

A license is binded to a machine given that the license generated contains the Instance ID of the device. This license will not be able to be used on other machines. 