---
layout: post
title: "Codis : A Redis Proxy"
date: 2015-02-18 10:04:03 +0800
comments: true
categories: ["redis"]
---

<!-- more -->

這星期看到`豌豆荚`分享他們怎麼設計 Redis 的架構，裡面提到他們使用 `Twemproxy` 和 reids cluster 的心得，
但是他們似乎都不太滿意因此自行撰寫了 [codis]。


[codis] 是用 C 和 GO 撰寫的 proxy，看起來類似 `Twemproxy`，不過他跟 `Twemproxy` 不一樣的地方在提供動態 `scale` 
和監控後台的功能，但是效能上開發人員說會慢 20% 左右。



[codis]:https://github.com/wandoulabs/codis