---
title: Bring the Gym Home!
keywords: integration
sidebar: userguide_fitness
permalink: userguide_fitness.html
folder: userguide
toc: false
---

------

## Setup

![](images/userguide/generic_fitness_setup.png)

In this setup, we have SpiderWare embedded in the Fitness Device device on the exercise equipment.

When switched ‘on’, the embedded SpiderWare will connect to the SpiderWare ExM Signaling server.

As a WebRTC solution, the SpiderWare ExM Signaling Server acts as an online ‘lobby server’ where connected SpiderWare clients can ‘see’ each other and initiate connections. Depending on the requirements of Fitness Device, there are two options for deploying the SpiderWare ExM Signaling Server:

- **Deployed in your Infrastructure** - Fitness Device may opt to own the SpiderWare ExM signaling Server and deploy it on their own infrastructure.
- **Deployed in EvoStream’s Infrastructure** - Fitness Device may opt to have the service deployed and managed in Evostream’s infrastructure.



## Customizing the ExM Signaling Server

A vanilla or barebones installation of ExM Signaling Server will enable you to experience all the features of the SpiderWare system.

But the beauty of this is that EvoStream can perform customization work on the ExM Signaling Server to match or enhance Fitness Device’s workflow.

![](images/userguide/exm_generic_fitness_setup-1.png)

In the diagram above, you see the online lobby function of the SpiderWare ExM Signaling Server subdivided into exercise categories (i.e. Cycling - Stationary Bikes, Running - Treadmill, and Cross Training). This is further subdivided into individual classes that could be assigned for specific trainers OR can be set up for ‘friends’.

![](images/userguide/exm_generic_fitness_setup-2.png)

Another possible setup would be to offer the Fitness Device device as a standalone system (unattached to an exercise machine). This device can then be used for general exercise classes like aerobics or rehabilitation/therapy.

In this setup, users can have separate sensors on their body (especially useful for rehabilitation/therapy), which are plugged into the Fitness Device device. The sensors can then be read by SpiderWare and shared to the trainer or therapist, etc.
