---
layout: post
title: "fastsocket"
date: 2014-11-14 21:29:46 +0800
comments: true
categories: ["linux"]
---


<!-- more -->


[fastsocket] 是由新浪和清華一起開發的專案，可以提高網路 IO 的效率，雖然是蠻新的專案但是從 Github 已經看到不少人關注，不過最主要的是
不需要更改上層應用程式的結構就可以使用這套系統，另外目前有新浪使用在生產環境下預計未來會慢慢提升使用率。

目前下面三個專案可以順利跑在 [fastsocket] 下。

    1. haproxy
    2. nginx (Do disable accept mutex)
    3. lighttpd



[fastsocket]:https://github.com/fastos/fastsocket