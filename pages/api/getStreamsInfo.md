---
title: getStreamsInfo
keywords: api
sidebar: api_sidebar
permalink: getStreamsInfo.html
folder: api
toc: false
---



Gets the current active streams

**Modules:** Core, WebRTC, RTSP, MP4



## API Parameter Table

| **Parameter Name** |       Type        | **Mandatory** | **Description**                                              |
| :----------------: | :---------------: | :-----------: | ------------------------------------------------------------ |
|     streamIds      | JSON array string |     false     | List of stream identifiers to query. A streamId is the unique identifier of a stream. It is unique for each stream in the server. |
|        name        |      string       |     false     | Name assigned to the stream/streams. It is expected that the stream name will not be unique. Outbound streams will adopt the name of the inbound streams. |
|     direction      |      string       |     false     | Direction filter. “**in**”\|”**out**” If present, the result will only contain inbound stream information. If this parameter is “**in**”, or outbound stream information if parameter is “**out**”. Parameter is ignored on invalid values |
|        type        |      string       |     false     | Module/stream type filter. The results will only contain info on streams that belong to a specific module/type. Parameter is ignored on invalid values. |



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/getStramsInfo
```

**Body**

    {    
    	"direction": "in",	
    	"type": "rtsp",
    	"
    }
### Sample API Call

```
http://127.0.0.1:9090/command/webrtc/getStramsInfo

{
    "direction": "in"
}
```



### Success Response in JSON

``` 
{
    "success": true,
    "result": {
        "streams": [
            {
                "streamId": "ST_1874f00e3c07",
                "name": "testStream",
                "direction": "in",
                "type": "rtsp",
                "path": "rtsp://167.179.70.95:5544/streamA",
                "video": {
                    "codec": "",
                    "width": 0,
                    "height": 0
                },
                "audio": {
                    "codec": "",
                    "mode": "",
                    "config": "",
                    "samplingFrequency": 8000,
                    "channels": 1
                },
                "stats": {
                    "video": {
                        "bytes": 0,
                        "packets": 0,
                        "bitRate": 0,
                        "aveBitRate": 0,
                        "frameRate": 0,
                        "aveFrameRate": 0,
                        "latency": 0
                    },
                    "audio": {
                        "bytes": 0,
                        "packets": 0,
                        "bitRate": 0,
                        "aveBitRate": 0,
                        "latency": 0
                    }
                }
            }
        ],
        "count": 1
    }
}
```



#### JSON Response

The JSON response contains the following details:

- status – **true** if the command was parsed and executed successfully, **false** if not.
- result - the stream details
  - streamID - stream identifier
  - name - stream name
  - direction - direction filter, “in”|”out”
  - type - module/stream type filter
  - path - URL of the stream source
  - video - video details
  - audio - audio details
  - stats - stream statistics

  ​

------

## Related Links

- [Record a Stream](userguide_record.html)