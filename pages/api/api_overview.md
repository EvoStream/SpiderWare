---
title: Overview
keywords: api
sidebar: api_sidebar
permalink: api_overview.html
folder: api
toc: false
---

## Transport protocol
The API command parameters are sent as a JSON payload in an HTTP 1.1 POST method, while the command and target module are found in the HTTP URL. SpiderWare’s HTTP port for API commands is configurable on config.json.

### API Request
The API Request has the following URL format:
``` 
http://<server-host>:<api-port>/command/<target-name>/<command-name>
``` 

**server-host:** valid hostname or accessible ip address of SpiderWare
**api-port:** pre-configured port for SpiderWare API calls
**target-name:** the name of the target module, e.g. webrtc, rtsp. If the target module is unknown, or the command is to be sent to the spiderware core, target-name should be core. If the target-name is core, SpiderWare will try to execute the command to all applicable modules and send the result as an aggregate.
**command-name:** specifies the name of the command to be called. All modules are not expected to support all commands.

The command parameters are enclosed in a JSON string inside the HTTP Body. An example of using JavaScript to send the command can be found at the appendix section.

### API Response
If target-name does not exist or a command-name is not implemented in the specified target-name, SpiderWare will return an HTTP 404 Error. Otherwise, API responses are sent as JSON payload in the corresponding HTTP 1.1 response message with a 200 OK status. 

***API Response Payload (to be implemented)***

|       **Key**      |  **Value Type**  | **Description**                                                             |
| :----------------: | :--------------: | --------------------------------------------------------------------------- |
|       success      |      boolean     | True if successful, false if there are errors                               |
|       result       |       JSON       | May be present when success is true. API result payload                     |
|      errorDesc     |      string      | May be present when success is false. Specifies the reason for the error    |


