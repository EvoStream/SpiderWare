---
title: SpiderWare Components
keywords: spiderware
sidebar: userguide_sidebar
permalink: userguide_spiderwarecomponents.html
folder: userguide
toc: true
---

------

## Structure

```

SpiderWare										>> Main Folder
	config										>> Configuration Folder
		config.json								>> Configuration File
	.init 										>> Initialization File
	EULA.pdf									>> End Users License Agreement fIle
	INFO										>> Build Information
	spiderware.exe/spiderware					>> SpiderWare Executable File
```

**config.json** - contains the configuration settings of SpiderWare. See [Configuration File](https://docs.google.com/document/d/1WahcEYitep7NA4SyQJJLdYIoqJSOLsw3ROlhsBsxLag/edit#heading=h.cak19tm1pqb)

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
    "version": "1.0.0",										>> SpiderWare Version
    "web": {
        "port": 9090,										>> Port number (SpiderWare)
        "docRoot": "../webroot"								>> Webroot Directory
    },
    "webrtc": {
        "user": "myemailt@mail.com",						>> Username
        "password": "password",								>> Username's Password
        "session": "mysession",								>> Session Name
        "signaling": "https://exm.evostream.com:5555"		>> Signaling Server URL
    },
    "sources": {
        "rtsp": "default"									>> ??
    }
}
```

**Note:** User, password, session are all set in ExM Manager.

