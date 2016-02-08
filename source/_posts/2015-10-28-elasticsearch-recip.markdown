---
layout: post
title: "elasticsearch recip function"
date: 2015-10-28 23:44:59 +0800
comments: true
categories: ["elasticsearch"]
---


<!-- more -->


在 elasticsearch 使用 script 實作 solr 的 recip function.


在	`config/script` 建立 `time_boost.groovy`，在 query time 引入 script_file 並且傳入現在時間。
