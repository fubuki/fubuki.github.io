---
layout: post
title: "lucene 索引格式"
date: 2015-08-03 23:27:09 +0800
comments: true
categories: ["algorithm"]
---


<!-- more -->

最近看了一些關於如何讓 `solr` 處理超大索引的研究，不過都沒有提到關於 lucene 索引格式的資料，
[Hacking Lucene - The Index format] 裡面有些資料結構是以前看過的，例如 `skip list` 之類的，由於
之後有可能需要更改或是把一些 lucenc/solr 在 jira 上的 patch 更有可能需要更改索引內容。


[Hacking Lucene - The Index format]:http://hackerlabs.org/blog/2011/10/01/hacking-lucene-the-index-format/