```
title: enterSessions
keywords: api
sidebar: api_sidebar
permalink: enterSessions.html
folder: api
toc: false

```

Joins a specific WebRTC session

**Modules:** WebRTC



## API Parameter Table

| **Parameter Name** | **Type** | **Mandatory** | **Description**                                            |
| :----------------: | :------: | :-----------: | ---------------------------------------------------------- |
|        host        |  string  |     true      | Signaling server host name                                 |
|     sessionId      |  string  |     true      | Session identifier                                         |
|      username      |  string  |     false     | List of username email addresses that can join the session |
|      password      |  string  |     false     | Username password                                          |



## API Call Template

```
http://<spiderwareIP>:9090/command/<module>/enterSessions
```

**Body**

```
{
  "host": "<host_ip>"
  "sessionId": "<sessionId>"  
}  
```



## Sample API Call

```
http://127.0.0.1:9090/command/webrtc/getSessions
```

```
{
  "host": "192.158.50.20"
  "sessionId": "xxxxxxxxx"  
}  
```



### Success Response in JSON

```
not yet implemented
```

#### JSON Response

The JSON response contains the following details:

- status – **true** if the command was parsed and executed successfully, **false** if not.
- users - list of user IDs which are currently in the session

------

## Related Links

- [getSession](getSession.html)
- [exitSession](exitSession.html)