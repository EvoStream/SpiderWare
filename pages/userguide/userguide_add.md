---
title: Adding Inbound Streams
sidebar: userguide_sidebar
permalink: userguide_add.html
folder: userguide
toc: true
---



## Adding Inbound RTSP Streams

To add an inbound stream, simply do the following:

1. Send an addStream-in command using RTSP module

   `http://localhost:9090/command/rtsp/addStream`

   ```
   {
       "type": "rtsp",
       "direction": "in",
       "path":"rtsp://167.179.70.95:5544/testStream",
       "name":"streamA"
   }
   ```

   ​

2. View the stream using the EXM server

   ​