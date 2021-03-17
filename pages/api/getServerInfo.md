---
title: getServerInfo
keywords: api
sidebar: api_sidebar
permalink: getServerInfo.html
folder: api
toc: false
---



Gets the SpiderWare instance information.

**Modules:** Core




## API Parameter Table
This function has no parameters.



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/getServerInfo
```



### Sample API Call

```
http://127.0.0.1:9090/command/core/getServerInfo
```



### Success Response in JSON

``` 
{
    "success": true,
    "result": {
        "buildVersion": "SpiderWare 1.1.4.3",
        "buildDate": "2020-08-10 12:11",
        "revision": "60e9929",
        "instanceId": "e+8OoysKN9fmpHYIIZ/eVdtjyv+w0e9hcGDY8vfCbpVzRU91zXAyXeszmWHfYQxu/Ubodb8S1TSZADqYFud+oTgw0l2cJQ==",
        "licenseId": "5f509edfff00000050c913"
    }
}
```



#### JSON Response

The JSON response contains the following details:

- status – **true** if the command was parsed and executed successfully, **false** if not.
- result - the result of the API call
  - buildVersion - the SpiderWare version
  - buildDate - the application build date
  - revision - GIT revision short hash where the build was compiled
  - instanceId - instance identifier
  - licenseId - ID of the license being used by the running instance
