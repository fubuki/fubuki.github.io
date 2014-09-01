---
layout: post
title: "Flickr 如何使用 redis 的 Sentinel"
date: 2014-08-20 23:42:05 +0800
comments: true
categories: ["redis"]
---

<!-- more -->

今天看到一篇關於Flicker 如何使用 redis sentinel 的文章 [Redis Sentinel at Flickr]， 裡面提到一些
我這邊沒有想過的和遇過的場景，之後擴展 redis 時可以參考避免掉一些問題。

另外 redis的作者針對文章做出回應 [Reply to Aphyr attack to Sentinel] ，下面就是作者在文章裡提出的當初開發出 Sentinel 的目的，
也知道會有 [Redis Sentinel at Flickr] 中提到的問題。

	Redis Sentinel is a distributed *monitoring* system, with support for automatic failover.

[Redis Sentinel at Flickr]:http://code.flickr.net/2014/07/31/redis-sentinel-at-flickr/
[Reply to Aphyr attack to Sentinel]:http://antirez.com/news/55

