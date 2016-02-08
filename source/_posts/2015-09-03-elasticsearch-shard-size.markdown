---
layout: post
title: "elasticsearch 適合的 shard size"
date: 2015-09-03 23:12:17 +0800
comments: true
categories: ["elasticsearch"]
---


<!-- more -->


最近在思考 elasticsearch 優化的部分，當 index 不斷擴大的時候怎麼處理，目前是想到將資料做
 shard 然後使用多個 node 加快搜尋的速度，但是這邊有個問題是每個 shard 的大小要怎麼決定，
 這邊就暫時參考 [Balancing an Elasticsearch Cluster by Shard Size] 裡面提到的指標和工具測試看看。


[Balancing an Elasticsearch Cluster by Shard Size]:http://engineering.datarank.com/2015/07/08/balancing-elasticsearch-cluster-by-shard-size.html
