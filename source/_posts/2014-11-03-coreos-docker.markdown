---
layout: post
title: "coreos docker"
date: 2014-11-03 21:06:19 +0800
comments: true
categories: ["docker"]
---


<!-- more -->

[coreos] 是基於 docker 可用來建立大型的運算平台的 linux 發行版本，從官網看來可以知道 coreos 是希望藉由建立群集然後在上面跑 docker 容器的方式
擴展整個平台， coreos 裡面除了有 docker 之外有兩個東西還蠻有趣的，一個是 etcd 另外一個是 fleet，這兩個都有開源在 github 上面。


#### etcd
etcd 類似 zookeeper 的東西能夠檢查伺服器是否存活，裡面使用了 Raft 的演算法。


#### fleet
[Cluster-Level Container Deployment with fleet]。


[Cluster-Level Container Deployment with fleet]:https://coreos.com/blog/cluster-level-container-orchestration/

[coreos]:https://coreos.com/