---
title: 微信小程序页面间事件通信错误Cannot read property emit of undefined
type: article
tag: 微信小程序
abbrlink: 399976084
date: 2020-06-30 00:00:00
---


#### 报错信息：
```handlebars
VM1836:1 thirdScriptError
Cannot read property 'emit' of undefined;at pages/board/board onReady function;at api navigateTo success callback function
TypeError: Cannot read property 'emit' of undefined
    at Function.success (http://127.0.0.1:17382/appservice/pages/board/board.js:32:26)
    at Object.success (http://127.0.0.1:17382/appservice/__dev__/WAService.js:3:14159)
    at u (http://127.0.0.1:17382/appservice/__dev__/WAService.js:4:6009)
    at http://127.0.0.1:17382/appservice/__dev__/WAService.js:4:6192
    at n.<anonymous> (http://127.0.0.1:17382/appservice/__dev__/asdebug.js:1:10293)
    at http://127.0.0.1:17382/appservice/__dev__/WAService.js:3:14159
    at http://127.0.0.1:17382/appservice/__dev__/WAService.js:8:25162
console.error @ VM1836:1
errorReport @ VM1843 WAService.js:3
thirdErrorReport @ VM1843 WAService.js:3
(anonymous) @ VM1843 WAService.js:3
u @ VM1843 WAService.js:4
(anonymous) @ VM1843 WAService.js:4
(anonymous) @ VM1840 asdebug.js:1
(anonymous) @ VM1843 WAService.js:3
(anonymous) @ VM1843 WAService.js:8
setTimeout (async)
setTimeout @ VM1843 WAService.js:8
(anonymous) @ VM1840 asdebug.js:1
(anonymous) @ VM1840 asdebug.js:1
(anonymous) @ VM1840 asdebug.js:1
_ws.onmessage @ VM1840 asdebug.js:1
VM1836:1 thirdScriptError
this.getOpenerEventChannel is not a function;at "pages/detail/detail" page lifeCycleMethod onLoad function
TypeError: this.getOpenerEventChannel is not a function
    at r.onLoad (http://127.0.0.1:17382/appservice/pages/detail/detail.js:17:29)
    at r.<anonymous> (http://127.0.0.1:17382/appservice/__dev__/WAService.js:18:24831)
    at D (http://127.0.0.1:17382/appservice/__dev__/WAService.js:18:1254)
    at F (http://127.0.0.1:17382/appservice/__dev__/WAService.js:18:2027)
    at K (http://127.0.0.1:17382/appservice/__dev__/WAService.js:18:3339)
    at Function.<anonymous> (http://127.0.0.1:17382/appservice/__dev__/WAService.js:18:6274)
    at http://127.0.0.1:17382/appservice/__dev__/WAService.js:18:12486
    at http://127.0.0.1:17382/appservice/__dev__/WAService.js:5:22695
    at Array.forEach (<anonymous>)
    at Function.<anonymous> (http://127.0.0.1:17382/appservice/__dev__/WAService.js:5:22675)
console.error @ VM1836:1
errorReport @ VM1843 WAService.js:3
thirdErrorReport @ VM1843 WAService.js:3
(anonymous) @ VM1843 WAService.js:3
(anonymous) @ VM1843 WAService.js:18
D @ VM1843 WAService.js:18
F @ VM1843 WAService.js:18
K @ VM1843 WAService.js:18
(anonymous) @ VM1843 WAService.js:18
(anonymous) @ VM1843 WAService.js:18
(anonymous) @ VM1843 WAService.js:5
(anonymous) @ VM1843 WAService.js:5
(anonymous) @ VM1843 WAService.js:4
o @ VM1840 asdebug.js:1
(anonymous) @ VM1840 asdebug.js:1
(anonymous) @ VM1840 asdebug.js:1
_ws.onmessage @ VM1840 asdebug.js:1
```
#### 解决：把本地设置里的调试库调高！！！
![调试库](20200630114436485.jpg)
