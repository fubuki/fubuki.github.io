---
layout: post
title: "hadoop lambda architecture"
date: 2014-10-05 22:16:59 +0800
comments: true
categories: ["hadoop"]
---

<!-- more -->

最近在研討會上看到一個 [Lambda Architecture] 讓 hadoop 分析一些 Streaming data ，說明在需要一些需要即時分析資料並且回傳到前端的程式的情形下，
資料處理速度需要非常快，因而採用了這樣一個架構， 目前我看到的組件是 hadoop 搭配 [storm]。


[Lambda Architecture]:http://lambda-architecture.net/
[storm]:https://storm.incubator.apache.org/