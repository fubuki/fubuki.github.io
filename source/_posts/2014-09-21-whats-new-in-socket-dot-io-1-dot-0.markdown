---
layout: post
title: "Socker.io 1.0 版本有哪些變動"
date: 2014-09-21 21:43:45 +0800
comments: true
categories: ["socketio"]
---

<!-- more -->


[What's new in Socket.IO 1.0]裡面介紹新版本的架構和哪些更動的地方，可以藉由這篇文章看出
Sockert.io 分成哪些部分。

1. engine.io
2. engine.io-client
3. engine.io-parser
4. socket.io
5. socket.io-adapter
6. socket.io-client
7. socket.io-parser
8. socket.io-protocol
9. socket.io-redis
10. socket.io-emitter

另外是關於 scale out 的問題，在 [Cluster fucks when scaling Socket.IO] 有提到一些作者覺得當 socket.io scale out 需要
考慮的事情，而在 1.0 版本裡面把 redis 的部分拆開了，可以換用其他方式實現 cluster 架構，在 [Scalability of socket.io 1.0 in Node.js cluster]
裡面有提到一些可以參考的例子。

[What's new in Socket.IO 1.0]:http://juriy.com/p/socket-io.html
[Cluster fucks when scaling Socket.IO]:https://medium.com/@3rdeden/cluster-fucks-when-scaling-socket-io-2c8ad1153332
[Scalability of socket.io 1.0 in Node.js cluster]:https://github.com/Automattic/socket.io/issues/1457