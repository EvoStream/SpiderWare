---
title: sendData
keywords: api
sidebar: api_sidebar
permalink: sendData.html
folder: api
toc: false
---

Sends metadata to a specific endpoint.

**Modules:**
Core, WebRTC




## API Parameter Table

| **Parameter Name** |  Type  | **Mandatory** |**Description**                                                                |
| :----------------: | :----: | :-----------: | ----------------------------------------------------------------------------- |
|        peerID      | string |     true      | The Peer ID of the WebRTC peer. Use **all** to send the data in all peers     |
|         data       | string |     true      | Metadata to send                                                              |




## API Call Template

``` 
http://spiderwareIP:9090/command/<module>/sendData
```
**Body**
``` 
{
"peerId": "<peerID",
"data": "<data to send>"
}
```



### Sample API Call

```
http://127.0.0.1:9090/command/webrtc/sendData

{
"peerId": "all",
"data": "Test Data"
}
```

This will send `Test Data` in all peers connected in the same session



### Success Response in JSON

``` 
{
    "success": true
}
```


#### JSON Response

The JSON response contains the following details:

- status – **true** if the command was parsed and executed successfully, **false** if not.


------

## Related Links

- [getPeerId](getPeerId.html)
