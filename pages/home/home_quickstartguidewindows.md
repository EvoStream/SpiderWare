---
title: Quick Start Guide on Windows
keywords: quick start guide
sidebar: home_sidebar
permalink: /home_quickstartguidewindows.html
folder: home
toc: true
---

## Purpose

This document provides instructions on how to install SpiderWare application on Windows operating systems.
The document also provide instructions for some basic features of the EMS such as installing and starting SpiderWare, adding and playing source streams and shutting down SpiderWare.



## Getting SpiderWare

1. Download the SpiderWare package installer at <https://spiderware.evostream.com/release/>
```
Username : spiderware
Password : wWCU4iTG#$c4Pfq@
```

2. Install SpiderWare

   2.1. Extract the zip package

   2.2. Right-click on `setup.exe` then click **Run as administrator**

   ​

   2.3. Click **Next** to continue the installation

   ![](images/userguide/install_1.JPG)

   ​

   2.4. Verify the installation path, click **Next**

   ![](images/userguide/install_2.JPG)

   ​

   2.5. Read the license agreement and select **I agree**, click **Next**

   ![](images/userguide/install_3.JPG)

   ​

   2.6. Click **Next** to confirm the installation

   ![](images/userguide/install_4.JPG)

   ​

   2.7. Click **Close** to finish the installation.

   ![](images/userguide/install_5.JPG)

   ​


## License Installation

**Note:** You should already have your license file available. If none, SpiderWare offers a **30-day free trial** license to those who want to explore the features of SpiderWare. Click [here](https://evostream.com/free-trial/) to avail the free trial or contact [salesupport@evostream](mailto:salessupport@evostream.com) for other license type purchase.

To install the license, simply copy the `License.lic` file to `C:\Program Files\SpiderWare`.


## Configuring SpiderWare
You can find the configuration file in `C:\Program Files\SpiderWare\config\config.json`


## Starting SpiderWare

To start SpiderWare, simply **double click on the shortcut icon** of SpiderWare or double click on `launch.bat` in the installed SpiderWare folder.

![](images/home/shortcut.JPG)


The shortcut icon calls the `spiderware.exe`. You may also run this executable found in the installed SpiderWare. Simply double-click to start the server. This script simply runs the application through the command prompt, using `spiderware.exe config\config.json license\license` as the main server configuration.
You can also double-click on `launch.bat`. This is simply a script that does the same. 
The SpiderWare will open a console:

![](images/userguide/start.JPG)



To check running applications, open the Task Manager and you should see:

```
SpiderWare by EvoStream
```


## Adding Source Stream
To add an RTSP source to SpiderWare, send the following HTTP POST request (assuming that SpiderWare and client used to send the command is on the same machine):
```
url: http://localhost:9090/command/rtsp/addStream
data: {
"type":"rtsp",
"direction":"in",
"path":"<rtsp source>",
"name":"<target stream name>"
}

```


For example, an RTSP source “rtsp://192.168.0.103:10000/test.sdp” is to be added and with a target stream name of “bunny”, using a cURL command would be:
```
curl --header "Content-Type: application/json" --request POST --data "{ \"type\":\"rtsp\", \"direction\":\"in\", \"path\":\"rtsp://192.168.0.103:10000/test.sdp\", \"name\":\"bunny\" }" http://localhost:9090/command/rtsp/addStream
```

   
## Stream Playback
To view the RTSP stream through webrtc with a demo page:
1. Using a browser, open https://exm.evostream.com/viewer/
2. Enter the session name on the input field that matches the session parameter on the config.json file that you received
3. Click on “Connect”
4. On the left pane of the demo page, select a stream from currently connected SpiderWare instances.




## Stopping SpiderWare

If the user wants to shut down the SpiderWare application, just send the command:

```
getServerInfo
```


Take note of the Instance ID, then send the shutdown command:


```
shutdownServer instanceID=<instanceID>
```

The SpiderWare will shut down after sending the command.



Please refer to [SpiderWare User Guide](http://docs.evostream.com/spiderware/userguide.html) and [SpiderWare API Guide](http://docs.evostream.com/spiderware/api_overview.html) for more information.

