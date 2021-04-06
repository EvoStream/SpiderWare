---
title: Quick Start Guide on Windows
keywords: quick start guide
sidebar: home_sidebar
permalink: /home_quickstartguidewindows.html
folder: home
toc: true
---

------

This document provides instructions on how to install SpiderWare application on Windows operating systems.
The document also provide instructions on installing and starting SpiderWare, adding and playing source streams and shutting down SpiderWare.



## Getting SpiderWare

1. Download the SpiderWare package installer at <https://spiderware.evostream.com/release/>
```
Username : spiderware
Password : wWCU4iTG#$c4Pfq@
```

2. Install SpiderWare

   2.1. Extract the zip package

   2.2. Right-click on `setup.exe` then click **Run as administrator**

   

   2.3. Click **Next** to continue the installation

   ![](images/home/install_1.JPG)

   

   2.4. Verify the installation path, click **Next**

   ![](images/home/install_2.JPG)

   

   2.5. Read the license agreement and select **I agree**, click **Next**

   ![](images/home/install_3.JPG)

   

   2.6. Click **Next** to confirm the installation

   ![](images/home/install_4.JPG)

   

   2.7. Click **Close** to finish the installation.

   ![](images/home/install_5.JPG)

   

   


## License Installation

**Note:** You should already have your license file available. If none, SpiderWare offers a **30-day free trial** license to those who want to explore the features of SpiderWare. Click [here](https://evostream.com/free-trial/) to avail the free trial or contact [salesupport@evostream](mailto:salessupport@evostream.com) for other license type purchase.

To install the license, simply copy the `License.lic` file to `C:\Program Files\SpiderWare`.





## Configuring SpiderWare

You can find the configuration file in `C:\Program Files\SpiderWare\config\config.json`






## Starting SpiderWare

To start SpiderWare, simply run the command below in terminal:

1. Open a terminal

2. Locate the SpiderWare folder

3. Run the command below

   ```
   spiderware.exe config\config.json license\License
   ```

   This will call the configuration file and validates the license in the given path

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



