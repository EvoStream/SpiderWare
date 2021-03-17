```
title: exitSessions
keywords: api
sidebar: api_sidebar
permalink: exitrSessions.html
folder: api
toc: false

```

Exits a specific WebRTC session

**Modules:** WebRTC



## API Parameter Table

| **Parameter Name** | **Type** | **Mandatory** | **Description**    |
| :----------------: | :------: | :-----------: | ------------------ |
|     sessionId      |  string  |     true      | Session identifier |



## API Call Template

```
http://<spiderwareIP>:9090/command/<module>/exitSessions
```

**Body**

```
{
  "sessionId": "<sessionId>"  
}  
```



## Sample API Call

```
http://127.0.0.1:9090/command/webrtc/exitSessions
```

```
{
  "users": "xxxxxxxxx"  
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

- [enterSession](enterSession.html)
- [getSession](getSession.html)

