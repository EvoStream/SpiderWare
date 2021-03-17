---
title: getSessions
keywords: api
sidebar: api_sidebar
permalink: getSessions.html
folder: api
toc: false
---

Retrieves the active sessions in an signaling server host

**Modules:** WebRTC



## API Parameter Table

| **Parameter Name** | **Type** | **Mandatory** | **Description**            |
| :----------------: | :------: | :-----------: | -------------------------- |
|        host        |  string  |     true      | Signaling server host name |



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/getSessions
```

**Body**
``` 
{
    "host": "<host_ip>"
}
```



## Sample API Call

``` 
http://127.0.0.1:9090/command/webrtc/getSessions

{
    "host": "192.168.50.20"
}
```



### Success Response in JSON

``` 
not yet implemented
```



#### JSON Response

The JSON response contains the following details:

- status – **true** if the command was parsed and executed successfully, **false** if not.
- sessions - list of active WebRTC session details
  - sessionId – session identifier
  - userCount– number of users connected to the session
  - security – list of implemented security mechanisms, e.g. user-pass auth, etc. May not be present if there is no security mechanism in place

------

## Related Links

- [enterSession](enterSession.html)
- [exitSession](exitSession.html)


