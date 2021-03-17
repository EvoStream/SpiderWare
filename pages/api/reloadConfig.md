---
title: reloadConfig
keywords: api
sidebar: api_sidebar
permalink: reloadConfig.html
folder: api
toc: false
---

Reloads configuration.

**Modules:** Core




## API Parameter Table


| **Parameter Name** |  **Type**  | **Mandatory** | **Description**                                     |
| :----------------: | :--------: | :-----------: | --------------------------------------------------- |
|     configPath     |   string   |     false     | If not declared, defaults to current path used      |
|   forceRestart     |   boolean  |     false     | Restarts the server after reloading configuration   |



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/reloadConfig
```
**Body**
``` 
{
   "configPath": "C:\\Program Files\\SpiderWare\\config\\config.json",
   "forceRestart": "true"
}
```



### Sample API Call

``` 
http://127.0.0.1:9090/command/core/reloadConfig
{
   "configPath": "C:\\Program Files\\SpiderWare\\config\\config.json",
   "forceRestart": "true"
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
