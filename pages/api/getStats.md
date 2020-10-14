---
title: getStats
keywords: api
sidebar: api_sidebar
permalink: getStats.html
folder: api
toc: false
---



Retrieves WebRTC statistics of a specified peer ID.

## Modules
Core, WebRTC


## API Parameter Table

| **Parameter Name** |  Type  | **Mandatory** | **Default Value** | **Description**                    |
| :----------------: | :----: | :-----------: | :---------------: | ---------------------------------- |
|        peerID      | string |     true      |      *null*       | The Peer ID of the WebRTC peer     |



## API Call Template

``` 
http://localhost:9090/command/core/getStats
```

**Body**
``` 
{
    "peerId": "Q3QidO7EoAY1xn01AAFV"
}
``` 



### Success Response in JSON

``` 
{
    "success": true,
    "result": {
        "peerId": "Q3QidO7EoAY1xn01AAFV"
    }
}
```



#### JSON Response

The JSON response contains the following details:

- peerID – ID of the WebRTC peer 
- local – Statistics of SpiderWare WebRTC connection
- remote – Present if applicable / available. Statistics of remote peer connection

------

## Related Links

- [getStreamInfo](getStreamInfo.html)

