---
title: shutdown
keywords: api
sidebar: api_sidebar
permalink: shutdown.html
folder: api
toc: false
---

Shuts down a specific running instance.

**Modules:** Core

## API Parameter Table

| **Parameter Name** |  **Type**  | **Mandatory** | **Description**                                                                 |
| :----------------: | :--------: | :-----------: | ------------------------------------------------------------------------------- |
|     instanceId     |   string   |     true      | Instance ID. It should match the instance ID of the API command destination     |
|        delay       |   integer  |     false     | Number of seconds before shutting down. 0 by default, which means immediately   |



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/shutdown
```

**Body**
``` 
{
"instanceId":"gF6G6uicvr8VRD/czmylQE0XNtFh7AwxOyZGvzU17VWNZMViBPE2DcZcKgU8RYyq3giWJeQ0gvaV5QhN9h7Bt2G1CCvqdw=="
}
```



### Sample API Call

``` 
http://<127.0..0.1>:9090/command/core/shutdown

{
"instanceId":"gF6G6uicvr8VRD/czmylQE0XNtFh7AwxOyZGvzU17VWNZMViBPE2DcZcKgU8RYyq3giWJeQ0gvaV5QhN9h7Bt2G1CCvqdw=="
}

```



### Success Response in JSON

``` 
{
    "success": true
}
```



#### JSON Response

The JSON response contains the following details:
- status – **true** if the command was parsed and executed successfully, **false** if not.




## Related Links

- [getServerInfo](userguide_getServerInfo.html)
