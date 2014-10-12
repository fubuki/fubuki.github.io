---
layout: post
title: "browserchannel"
date: 2014-03-04 21:42:03 +0800
comments: true
categories: ["browserchannel"]
---

google版的socketio，用於gmail和google doc的部分。  

<!-- more -->
[node-browserchannel][]   

  [node-browserchannel]: https://github.com/josephg/node-browserchannel   "node-browserchannel"

需要稍微測試一下與sockeio之間的不同點。

記錄一下sever-side的參數

defaultOptions = {
  hostPrefixes: null,
  base: '/channel',
  keepAliveInterval: 20 * 1000,
  sessionTimeoutInterval: 30 * 1000,
  cors: null,
  corsAllowCredentials: false,
  headers: null
};