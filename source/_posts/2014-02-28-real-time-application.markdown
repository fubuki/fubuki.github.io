---
layout: post
title: "real-time-application"
date: 2014-02-28 20:26:17 +0800
comments: true
categories: nodejs
---

*** nodejs + socket.io + redis ***
----------------------------------
使用nodejs當 notification server，redis當message server，  
socket.io連接web browser推送訊息給前端。

對手機目前使用node-gcm推送給手機  

redis沒有辦法暫存資料，需要使用類似rabbitmq的message queue 替代  