---
layout: post
title: "如何使用 Groupcache"
date: 2015-04-16 22:31:29 +0800
comments: true
categories: ["golang"]
---

<!-- more -->

### Groupcache 與 memcached 的差別
同樣都是由相同作者開發的，只是 memcached 是使用 C++ 而 [groupcache] 是使用 golang 開發的，
然後 memcached 是作為獨立一個程式運作的，但是 [groupcache] 本身就是 `client library` 和 `server`，
使用起來反而比較像 sqlite。 

### 如何使用 Groupcache




[groupcache]:https://github.com/golang/groupcache