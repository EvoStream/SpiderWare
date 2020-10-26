---
title: addStream
keywords: api
sidebar: api_sidebar
permalink: addStream.html
folder: api
toc: false
---

Attempt to establish an inbound or outbound stream.

**Modules:** Core, RTSP, MP4


## API Parameter Table


| **Parameter Name** |  **Type**  | **Mandatory** | **Description**                    |
| :----------------: | :--------: | :-----------: | ---------------------------------- |
|        type        |   string   |     true      | Transport name or container name, e.g. “rtsp”, “mp4”      |
|      direction     |   string   |     true      | Describes the stream direction in the server’s perspective. Value allowed are “in” and “out”.       |
|        path        |   string   |     true      | Path to where the stream will be coming (in) or going (out). It could be a URL, path to file or device, depending on the protocol   |
|        name        |   string   |     false      | Arbitrary name for the stream. Whitespaces are prohibited. On *incoming streams*, it is the name to be assigned for reference. If missing, the generated unique stream identifier will be its name. On *outgoing streams*, it is the name that can be used to reference streams.           |


### Module Specific Parameters
| **Parameter Name** |  **Type**  | **Mandatory** | **Description**                    |
| :----------------: | :--------: | :-----------: | ---------------------------------- |
|  targetStreamName  |   string   |     true      | Mandatory, on direction=out. Stream name that is expected by the receiving end      |
|     rtpTransport   |   integer  |     false     | Applicable only when direction is in. Optional, defaults to 0. Valid values are: 0 - UDP Unicast, 1 - UDP MultiCast, 2 - Over TCP, 3 - Over HTTP   |
|     timeout   |   integer  |     false     | The number of seconds to wait before the rtsp connection attempt times out. Optional, defaults to 5.    |

**Note:**
Direction "out" is not supported in MP4 module.


## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/addStream
```

**Body**
``` 
{
    "type": "<module>",
    "direction": "<direction>",
    "path":"<source stream URL",
    "name":"<stream name>"
}
``` 



### Sample API Call

``` 
http://127.0.0.1:9090/command/rtsp/addStream

{
    "type": "rtsp",
    "direction": "in",
    "path":"rtsp://167.179.70.95:5544/testStream",
    "name":"testStream"
}

```


### Success Response in JSON

``` 
{
    "success": true,
    "result": {
        "streamId": "ST_4d4c25027f03"
    }
}
```



#### JSON Response

The JSON response contains the following details:

- status – **true** if the command was parsed and executed successfully, **false** if not.
- result - the result of the API call
    - streamId - the name assigned to the stream. If missing, the generated unique stream identifier will be its name

------

## Notes

- Direction "out" is not supported in MP4 module.


------

## Related Links

- [mediaStorage](userguide_confuglua.html#mediastorage)
- [listStorage](listStorage.html)
- [removeStorage](removeStorage.html)

