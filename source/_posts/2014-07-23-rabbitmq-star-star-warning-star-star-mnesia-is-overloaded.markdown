---
layout: post
title: "RabbitMQ ** WARNING ** Mnesia is overloaded"
date: 2014-07-23 00:54:47 +0800
comments: true
categories: ["rabbitmq"]
---

大坑待補  

<!-- more -->

在使用 `rabbitmq` 的時候出現一些奇怪的問題，可以連線但是無法訂閱 `topic`，還有 rabbitmq 關機跟開機很慢的問題，
看 log 有一段是 `** WARNING ** Mnesia is overloaded"` ，網路上搜尋也有不少人有同樣的問題，在這邊記錄一下解法
在測試看看行不行。

  
[Q-Mnesia-is-overloaded-td2098730]  
[How to Eliminate Mnesia Overload Events]  

[Q-Mnesia-is-overloaded-td2098730]: http://erlang.2086793.n4.nabble.com/Q-Mnesia-is-overloaded-td2098730.html
[How to Eliminate Mnesia Overload Events]: http://streamhacker.com/2008/12/10/how-to-eliminate-mnesia-overload-events/