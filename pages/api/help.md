---
title: help
keywords: api
sidebar: api_sidebar
permalink: help.html
folder: api
toc: false
---



Get information on a specific or all commands.

**Modules:** Core, WebRTC, RTSP, MP4


## API Parameter Table


| **Parameter Name** |  Type  | **Mandatory** | **Description**                    |
| :----------------: | :----: | :-----------: | ---------------------------------- |
|       command      | string |     false     | If this parameter is present, the result will only give information on this specific command. If not, information on all available commands in the stated module is given.      |



## API Call Template

``` 
http://<spiderwareIP>:9090/command/<module>/help
```

**Body**
``` 
{
    "command": "<Command API>"
}
``` 


## Sample API Call
``` 
http://localhost:9090/command/core/help

{
    "command": "shutdown"
}
```



### Success Response in JSON

``` 
{
    "success": true,
    "result": {
        "commands": [
            {
                "name": "shutdown",
                "params": [
                    {
                        "name": "instanceId ",
                        "type": "String",
                        "desc": "Instance ID. It should match the instance ID of the API command destination.",
                        "required": true
                    },
                    {
                        "name": "delay",
                        "type": "int",
                        "description": "Number of seconds before shutting down. 0 by default, which means immediately",
                        "required": true
                    }
                ],
                "description": "Shuts down a specific running instance.",
                "module": "core"
            }
        ]
    }
}
```



#### JSON Response

The JSON response contains the following details:

- status – **TRUE** if the command was parsed and executed successfully, **FAIL** if not.
- result – The list of commands
  - command – The list of command information
    - name – Command name
    - params - List of parameters
         - name - Parameter name
         - type – Parameter value type
         - description – Describes the use of the parameter
         - required - Parameter requirement
     - description – API description
     - module – Supporting module name

------

