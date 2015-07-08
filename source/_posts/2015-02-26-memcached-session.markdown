---
layout: post
title: "memcached session 問題"
date: 2015-02-26 23:46:27 +0800
comments: true
categories: ["memcached"]
---

<!-- more -->

使用 memcached 存放 session 有可能遇到的問題，可以了解一下 memcached 內部的機制，Slab , Page, Chunk 分別代表的意義。

1. [Sessions in Memcached]
2. [dormando - Cache your sessions. Don't piss off your users]


[Sessions in Memcached]:http://www.dormando.me/articles/memcached_sessions/
[dormando - Cache your sessions. Don't piss off your users]:http://dormando.livejournal.com/495593.html