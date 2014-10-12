---
layout: post
title: "redis 的 Bitmap 和 HyperLogLogs"
date: 2014-10-09 23:36:30 +0800
comments: true
categories: ["redis"]
---

<!-- more -->

redis 之前新增了兩個資料類型 : Bitmap 和 HyperLogLogs，現在特別紀錄一下這兩種類型的差別和用途。

### Bitmap

Bitmap 似乎是讓 string 類型可以有 bit 層級的操作命令，目前看起來可以用在紀錄會員活耀數。



### HyperLogLogs

HyperLogLogs 用來做基数估计的演算法，藉此可以用來做大數據分析。

[Sketch of the Day: HyperLogLog — Cornerstone of a Big Data Infrastructure]

[Sketch of the Day: HyperLogLog — Cornerstone of a Big Data Infrastructure]:http://research.neustar.biz/2012/10/25/sketch-of-the-day-hyperloglog-cornerstone-of-a-big-data-infrastructure/