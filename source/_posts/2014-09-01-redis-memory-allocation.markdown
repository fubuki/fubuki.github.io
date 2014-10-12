---
layout: post
title: "redis memory allocation"
date: 2014-09-01 23:42:58 +0800
comments: true
categories: ["redis"]
---

<!-- more -->

redis 記憶體分配器，redis 不知道從哪一個版本開始是預設使用 jemalloc，據說效能比預設的 glibc 的還要高，
另外在網路上有人提到使用 TCMalloc 提高 nginx 和 redis的效能。


1. jemalloc
2. TCMalloc
3. glibc