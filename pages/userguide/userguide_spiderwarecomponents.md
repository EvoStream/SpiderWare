---
title: SpiderWare Configuration
keywords: spiderware
sidebar: userguide_sidebar
permalink: userguide_spiderwareconfiguration.html
folder: userguide
toc: true
---

------

## Structure

```
SpiderWare 
	config 
		config.json 
	.init 
	EULA.pdf 
	INFO
	spiderware.exe/spiderware
```

**config.json** - contains the configuration settings of SpiderWare.

**.init**- generated on the first run of SpiderWare. This is used to bind a license into the machine

**EULA.pdf** - please refer to the PDF file installed 

**INFO** - contains the build information of the SpiderWare application

```
Product Name: SpiderWare
Version: 1.0.0.0
Target Platform: Windows
Build date: 2020-07-09 06:19
Revision: a56ebd6
```

**SpiderWare Executable File** - run this file to start SpiderWare



## Configuration File

The config.json file is the configuration file used in SpiderWare

```
{
    "version": "1.0.0",
    "web": {
        "port": 9090,
        "docRoot": "../webroot"
    },
    "webrtc": {
        "user": "myemailt@mail.com",
        "password": "password",
        "session": "mysession",
        "signaling": "https://exm.evostream.com:5555"
    },
    "sources": {
        "rtsp": "default"									
    }
}
```

**version** - the SpiderWare application version

**port** - the port number used by the SpiderWare application

**docRoot** - the webroot directory

**user** - the email to be used in for the WebRTC communication

**password** - the password set for the user

**session** - the session name where the SpiderWare will join to

**signaling** - the URL of the signaling server to be used 



**Note:** User, password, session are all set in ExM Manager.

