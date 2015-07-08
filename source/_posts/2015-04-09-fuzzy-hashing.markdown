---
layout: post
title: "Fuzzy Hashing And ssdeep"
date: 2015-04-09 22:03:11 +0800
comments: true
categories: ["algorithm"]
---

<!-- more -->


最近在研究 webshell 的時候，有提到關於如何偵測 webshell 的方法，其中有介紹一種叫 `Fuzzy Hashing`
的演算法，一般像 md5 的 hash 方法只要文件有一些變化計算出來的數值就有很大的改變，這樣不利於檢查兩
份文件的相似度，所以才有 `Fuzzy Hashing`。

而 ssdeep 則是實現 `Fuzzy Hashing` 的程式，所以可以直接拿來測試手上的加殼程式，來看看效果如何。
