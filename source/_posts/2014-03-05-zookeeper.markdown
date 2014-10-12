---
layout: post
title: "zookeeper"
date: 2014-03-05 21:16:55 +0800
comments: true
categories: ["zookeeper"]
---

Apache Zookeeper 一開始是用在hadoop上面，原本hadoop是 master-slave的架構會有單點故障的問題，  
如果master掛點那就不用玩了，所以用zookeeper去監控各個節點當master故障就可以啟動災難復原，
