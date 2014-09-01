---
layout: post
title: "Erlang分布式開發"
date: 2014-08-25 23:35:02 +0800
comments: true
categories: ["erlang"]
---

<!-- more -->

今天看完 Erlang教程的快速入門，對照之前研究 rabbitmq 的經驗很快就上手了，參照網路上的說明
寫了一個範例，也看到 Erlang 在建立多個 Process 和通信上都很容易達成，另外也了解到 rabbitmq
 如何透過 .erlang.cookie 讓各個節點形成一個 cluster 的群集。