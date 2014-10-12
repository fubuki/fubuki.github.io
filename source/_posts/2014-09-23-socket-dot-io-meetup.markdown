---
layout: post
title: "Socket.IO Meetup"
date: 2014-09-23 23:51:07 +0800
comments: true
categories: ["socketio"]
---

在日本的一場跟 Socket.IO 有關的會議。

<!-- more -->
[影片]  

在尋找跟 socket.io-adapter 相關的資訊的時候找到的，[Socket.IO Meetup] 有邀請到 socket.io 的作者 `Guillermo`，
裡面有些 LT 很蠻有趣的， 然後重點在於 `Guillermo` 的 keynote，需要尋找一下演講內容。



### MQTT.IO
[MATT.IO]

### socket.io on SmartFx

投影片在這 [socketio-on-smartfx]，似乎是跟 FX 有關的公司，利用 socket.io 更新前端的資料，投影片裡面有寫他們是用 [socket.io-reqev] 開發的，
包裹 socket.io 的 framework，裡面比較有趣的部分是 socket.io 會將自身的狀態更新到資料庫然後 web server 會從 DB 裡面隨機選出一個 socket.io的連結給 client。


### Web-based multitrack recording

[WebMTR]

### Socket.IO 1.0 Client For Java

[Socket.IO 1.0 Client for Java]



[WebMTR]:https://github.com/kuu/WebMTR
[Socket.IO Meetup]:http://connpass.com/event/6911/
[影片]:http://www.ustream.tv/recorded/49506480
[MATT.IO]:https://speakerdeck.com/hakobera/mqtt-dot-io
[Socket.IO 1.0 Client for Java]:https://speakerdeck.com/nkzawa/socket-dot-io-1-dot-0-client-for-javafalseshao-jie
[socketio-on-smartfx]:http://www.slideshare.net/ssuser69ee9b/socketio-on-smartfx
[socket.io-reqev]:https://github.com/takeshy/socket.io-reqev