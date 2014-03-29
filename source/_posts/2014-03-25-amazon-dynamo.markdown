---
layout: post
title: "Amazon  Dynamo"
date: 2014-03-25 21:40:25 +0800
comments: true
categories: ['nosql']
---

amazon的 Dynamo架構值得參考，目前常看到的scale機制分成master-slave和Dynamo兩種架構，不過通常master-slave需要
類似zookeeper的機制另外監控，Dynamo卻不需要，必須比較一下兩者之間的差別。