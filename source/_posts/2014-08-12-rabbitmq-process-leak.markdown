---
layout: post
title: "rabbitmq process leak"
date: 2014-08-12 23:51:41 +0800
comments: true
categories: ["rabbitmq"]
---

<!-- more -->

Rabbitmq server 不定期會當機，經過長時間觀察，發現是 erl process 不正常增長的關係， connection 的數量
很正常但是 consumer 和 channel 的數量多出好幾倍，然後 queue的數量也不太對， 目前看得出來是 rabbitmq 的
other process 所佔的記憶體大小超過設定的記憶體上限並且將主機的記憶體整個吃滿，導致 rabbitmq 整個 crash。

目前運行的時候是一個 connecion 對應一個 channel 和 consumer 目前猜這是不是 queue 過多或是後端一次丟太多
訊息讓 rabbitmq 來不及處理的關係還需要一段時間觀察。
