---
layout: post
title: "memcached 的 lru_crawler"
date: 2015-03-28 22:02:57 +0800
comments: true
categories: ["memcached"]
---


<!-- more -->


最近在看 `memcached` 的原始碼看到一個  `lru_crawler` 的東西，這個東西是為了清除過期的資料存在的，但是一般是不會啟動這個功能，
會有這東西是因為 `memcached` 的資料在過期的時候不會立即清除，因此記憶體空間不會立即釋放，但是可以透過 `lru_crawler` 去遍歷 item
然後清除過期的 item。


另外 `memcached` 的官網有個有去的訊息 [Work In Progress LRU rework]，是替換關於 LRU 的部分目前在測試中。

[Work In Progress LRU rework]:https://github.com/memcached/memcached/pull/97