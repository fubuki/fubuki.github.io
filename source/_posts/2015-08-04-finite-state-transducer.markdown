---
layout: post
title: "FST AND FSA"
date: 2015-08-04 23:00:52 +0800
comments: true
categories: ["algorithm"]
---

<!-- more -->


在使用 Lucene 的時候看到在 4.0 增加了 FST 的方式處理自然語言，之前在自然語言處理綜論這本書上有看到關於 FST 的概念，
其實就是 FSM ，這邊有一個使用 FST 的專案 [SolrTextTagger] 是在一份關於如何處理多語言環境的簡報上看到的，剛好有這些契機，
而且似乎可以用 FST 處理關於同義詞的問題，正好可以拿來研究。

[SolrTextTagger]:https://github.com/OpenSextant/SolrTextTagger