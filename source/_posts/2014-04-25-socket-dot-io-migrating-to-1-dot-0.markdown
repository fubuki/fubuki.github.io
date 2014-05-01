---
layout: post
title: "Socket.io Migrating to 1.0"
date: 2014-04-25 22:47:54 +0800
comments: true
categories: ["socket.io"]
---

socket.io 已經有1.0版本了，所以免不了會有些大改動，wiki上面有一篇[Migrating-to-1.0]可以參考，這邊就記錄
目前程式升級有影響的部分。
<!-- more -->

## Authentication differences
以前在作認證的時候是透過`authorization`這個事件，在建立socket.io連線根據cliet端傳回的參數作處理。

	io.set('authorization', function (handshakeData, callback) {
  
	});

現在有'io.use()'這個方法，在socket建立的時候執行傳入的函式。

	io.use(function(socket, next) {
  		var handshakeData = socket.request;
  		// make sure the handshake data looks good as before
  		// if error do this:
    		// next(new Error('not authorized');
  		// else just call next
  		next();
	});

## Starting the server
以前會使用listen但是在1.0版本就不用了。

	var io = require('socket.io').listen(server);
vs
  
	var io = require('socket.io');
	var socket = io({ /* options */ })

## Exposed Events
似乎有些舊版的事件在新版(1.0)就消失或是使用其他事件取代。  
裡面有提到一個socket.io-client manager (lib/manager.js)值得研究，以前沒有注意這個東西。

## Configuration differences
以前設定socket.io的參數是用set之後是直接丟給socket.io。  

	io.set(
		'store' ,new RedisStore({
			redisPub : pub,
			redisSub : sub,
			redisClient : client
		})
	);

vs

	var socket = require('socket.io')({
  		// options go here
	});


## socket.io-adapter
原本在0.9版本之前有`store`的選項，到1.0版本之後就拿掉了換成`adapter`，然後官方有放出[socket.io-adapter]讓開發者可以
自行擴展，另外有一個[socket.io-redis]是官方放出來的參考範例，使用方法如下面所述。

	var socketio = require('socket.io');
	var RedisStore = require('socket.io-redis');
	var io = socketio(3000, {});
	io.adapter(RedisStore({ host: host, port: port }));

這邊有一個參考的簡報[socketio-10-25438209]



[socket.io-adapter]: https://github.com/LearnBoost/socket.io-adapter
[socket.io-redis]: https://github.com/Automattic/socket.io-redis
[Migrating-to-1.0]: https://github.com/LearnBoost/socket.io/wiki/Migrating-to-1.0
[socketio-10-25438209]:http://www.slideshare.net/lagos.jp/socketio-10-25438209