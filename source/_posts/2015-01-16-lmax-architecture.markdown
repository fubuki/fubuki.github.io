---
layout: post
title: "LMAX architecture"
date: 2015-01-16 22:37:48 +0800
comments: true
categories: ["architecture"]
---

<!-- more -->


[The LMAX Architecture] 一個高吞吐量的金融交易平台，是由 LMAX Exchange 基於 JVM 所建立的架構，文章裡面提到一些他們如何做到每秒六百萬訂單的
方法，另外這邊有 [LMAX - How to Do 100K TPS at Less than 1ms Latency] 文章作者的演講。

1. Event Source 
2. 全都在記憶體裡面運算
3. 由於 Event Source 的關係要另外處理持久化的問題
4. Disruptor 的 RingBuffer 結構



[The LMAX Architecture]:http://martinfowler.com/articles/lmax.html
[LMAX - How to Do 100K TPS at Less than 1ms Latency]:http://www.infoq.com/presentations/LMAX