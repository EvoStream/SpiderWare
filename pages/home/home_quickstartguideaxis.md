---
title: Quick Start Guide on Axis Camera
keywords: axis
sidebar: home_sidebar
permalink: /home_quickstartguideaxis.html
folder: home
toc: true
---

------

This document provides instructions on how to install SpiderWare application on a Axis Camera.
The document also provide instructions on installing and starting SpiderWare, playing source stream and shutting down SpiderWare.



## Prepare the Axis Camera

### Update the Firmware

1. Connect to the camera's web interface
2. Go to **System** > **Maintenance** > **“Firmware upgrade”**
3. Check if firmware needs to be updated
4. [IF NEEDED] Download the corresponding firmware for the camera
5. [IF NEEDED] Check the integrity of the file using sha256sum
6. [IF NEEDED] Select the correct firmware and hit **“upgrade”**
7. [IF NEEDED] Wait for camera to restart

**Note:** minimum firmware support is from **x.x**



### Enable SSH

1. Connect to the camera's web interface
2. Go to **“Plain config”** > **Network** > **SSH**
3. Tick the **“SSH Enabled”** option
4. Click on the **Save** button
5. Restart the camera if needed



## Install SpiderWare

1. Download the SpiderWare package installer for Axis at <https://spiderware.evostream.com/release/>
```
Username : spiderware
Password : wWCU4iTG#$c4Pfq@
```

2. Install SpiderWare

   2.1. Connect to the camera's web interface

   2.2. Go to **Settings > Apps > Add** 

   2.3 Select the SpiderWare package (.eap)

   2.4 Click Install

   **Note:** You will see the SpiderWare application under Apps if successfully installed.

   ![](images/home/installedswinaxis.png)

   

## License Installation

**Note:** A demo license is already installed along with the SpiderWare package. If you wish to change your license, replace the installed license at 





## Configuring SpiderWare

You can find the configuration file in `C:\Program Files\SpiderWare\config\config.json`






## Starting SpiderWare

To start SpiderWare, simply run the command below in terminal:

```
spiderware.exe config\config.json license\license
```

![](images/home/shortcut.JPG)


This will call the configuration file and validates the license in the given path

![](images/userguide/start.JPG)



To check running applications, open the Task Manager and you should see:

```
SpiderWare by EvoStream
```





## Stream Playback

To view the stream through WebRTC with a demo page:
1. Using a browser, open https://exm.evostream.com/
2. Enter the session name on the input field that matches the session parameter on the config.json file that you received
3. Click on “**Connect**”
4. On the left pane of the demo page, select a stream from currently connected SpiderWare instances.




## Stopping SpiderWare

If the user wants to shut down the SpiderWare application, simply press **CTRL+C**, enter **Y** to confirm.

```
Are you sure you want to exit? Y/N:
```



