---
title: Starting ExM
keywords: exm
sidebar: exmguide_sidebar
permalink: exmguide_startexm.html
folder: exm
toc: false
---

------

To start ExM, all you need to do is to go to the folder where ExM is installed.

### If installed via NPM

```
cd ~/exm
./node_modules/.bin/startexm
```



### If installed via Tarball

```
cd ~/exm
node index.js
```



**Note:** If you used port 80 and/or 443 for the ExM Frontend Demo Page, you may need to use **sudo** to start ExM.



### Daemonizing

If you wish to run ExM as a Daemon, we highly recommend you install and use [PM2](https://pm2.keymetrics.io/). Alternatively, you may also use **nohup**.