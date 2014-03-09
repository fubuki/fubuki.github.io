---
layout: post
title: "sockeio 使用心得"
date: 2014-03-09 15:57:12 +0800
comments: true
categories: nodejs
---

記錄一下到目前使用socket.io遇到的問題。

<!-- more -->

使用上是搭配redis對web做出即時推送服務，socket.io會自己幫我們做好與web溝通的部分，接下來就只是
事件驅動的部分。 比較有問題是在於scale out 的部分。

之前使用cluster功能讓nodejs能夠使用到多核心cpu的效能，不過socket.io會重復送出訊息，每個node會跟
redis 訂閱訊息，才會發生這樣的情形，官網上是有用提供一個方案讓各個node透過redis溝通，就不會有上述的
問題發生，不過尚未在高併發的環境下測試，也許會有其他問題。

The Trello Tech Stack 這篇文章最後有提到以下的事情:

> The Socket.io server currently has some problems with scaling up to more than 10K simultaneous client connections when using multiple processes and the Redis store, and the client has some issues that can cause it to open multiple connections to the same server, or not know that its connection has been severed. There are some issues 
with submitting our fixes (hacks!) back to the project – in many cases they only work with WebSockets (the only Socket.io transport we use). We are working to 
get those changes which are fit for general consumption ready to submit back to the project.

不過這篇[文章]是2012年的事情，還需要仔細研究一下。
[文章]: http://blog.trello.com/the-trello-tech-stack/   
