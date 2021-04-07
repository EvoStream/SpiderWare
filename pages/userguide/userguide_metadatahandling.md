---
title: BodyCam and DashCam
keywords: metadata
sidebar: userguide_bodydashcam
permalink: userguide_bodydashcam.html
folder: userguide
toc: false
---

------

![](images/userguide/spiderwarebodydash.jpg)



## Setup

### Dash Camera

Equipped with a GPS and a mobile connection, and running an embedded version of SpiderWare. The Dashcam could be installed on a patrol car or a delivery truck.

SpiderWare allows a client application to establish a WebRTC peering session with the Web Application client. During the peer session, SpiderWare can send a traditional Video and Audio stream back to the client.

Since WebRTC supports two way streaming, the user of the application can also stream something back to the Dashcam. For instance, if the Dashcam is equipped with a speaker, it can be used to playback audio feedback from the client viewer.

At the same time, SpiderWare can also stream sensor data such as GPS, telemetry and and other statistics back to the client. The additional data can be utilized to provide a richer user experience for the client. For instance, GPS data can be leveraged to show a real time map with the approximate position and direction of the vehicle.



### Body Camera

As with the Dashcam, the Bodycam be equipped with a GPS and a mobile connection, and running an embedded version of SpiderWare. This will be worn by a law enforcement officer while on mission.

SpiderWare allows a client application to establish a WebRTC peering session with the Web Application client. During the peer session, SpiderWare can send a traditional Video and Audio stream back to the client with the lowest possible latency.

As with the Dashcam use-case, the viewer can take advantage of the two-way streaming by sending audio streams back to the Bodycam.

Data is sent in parallel with the stream in the form of GPS, telemetry and and other the officer's vital statistics (assuming the bodycam can capture such data) back to the client.



## Workflow

SpiderWare is embedded on the dashcam and/or bodycam devices. It can be configured on active mode or passive mode: wherein it can either continuously send stream to the central server (active mode), or only send stream when playback is requested (passive mode). Streams are sent out with the lowest latency possible using the latest WebRTC specifications.

The bodycam/dashcam devices will require minimal configuration when in use, since it will automatically connect to SpiderWare’s exchange server. If additional changes in settings are required, it can be configured remotely as needed.

To prevent any loss of quality and crucial video data, the bodycam/dashcam will continuously record video into its local storage. The said devices will then automatically upload the recorded files when it has detected a direct peering to the central server.

While video/audio streams are being sent out, continuous delivery of metadata can be enabled that allows sending of GPS, accelerometer, and other applicable device/sensor data to the central server. For scenarios where the lowest latency playback is desired, the feature Priority View can be activated: where the playback directly connects to the devices, bypassing the central server, and allowing a true peer to peer connection with the devices.

In all cases, metadata such as GPS location, are continuously sent to the central server that allows real time monitoring, geo tagging, and plotting of the “spider-enabled” devices on an interactive map. These “moving points” can then be selected to view the corresponding video streams.



## Features

- Reliable and robust SRTP playback with minimal latency
- Updated logging mechanism for ease of parsing, reporting, and archiving
- Up to date WebRTC features and enhancements
- On & Go (auto connect and minimal configuration capability)
- Automated backup synchronization
- Metadata delivery
- Priority View (direct viewing of device camera)
- Recording capabilities and a companion video management system
- Geo tagging