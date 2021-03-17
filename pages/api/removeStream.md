---
title: removeStream
keywords: api
sidebar: api_sidebar
permalink: removeStream.html
folder: api
toc: false
---

Terminates and disconnects a specific stream. 

**Modules:** Core, WebRTC, RTSP, MP4



## API Parameter Table

| **Parameter Name** | **Type** | **Mandatory** | **Description**                                              |
| ------------------ | -------- | ------------- | ------------------------------------------------------------ |
| streamID           | string   | true          | Stream identifier.                                           |
| name               | string   | true          | Stream name.                                                 |
| type               | string   | true          | Stream type.  The parameter **type** is mandatory when the target module is core. Otherwise, it assumes the target module as type when that parameter is missing. |
| direction          | string   | true          | Direction of stream with respect to the server. “in”\|”out”  |

The primary basis for stream selection will be the **streamId**. When this is present, **name**, **type**, and **direction** will be ignored. If the **streamId** is not present, **name**, **type**, and **direction** should be present.



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/removeStream
```

**Body**

```
{
    "streamId": "ST_63e8e86da5a2"
}
```



### Sample API Call

``` 
http://127.0.0.1:9090/command/webrtc/removeStream

{
    "streamId": "ST_63e8e86da5a2"
}
```



### Success Response in JSON

``` 
{
    "success": true,
    "result": {
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

------

## Notes

- If you wan't your recorded file to start at the very beginning of the stream, issue the record first before `pullStream` command


------

## Related Links

- [Record a Stream](userguide_record.html)