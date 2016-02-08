---
layout: post
title: "php 使用 gcc 的 pgo 優化"
date: 2015-12-14 21:52:28 +0800
comments: true
categories: ["php"]
---


<!-- more -->

[Profile-guided optimization (PGO)] 為 GCC 的一個功能，可以藉由訓練優化編譯出來的程式，所以在網路上看到有人用
PGO 優化 PHP 的性能，不過實際上還要測試一下能增加多少性能，一般來說通常會開 opcache 優化如果比較起來相差不大
也許也不用特地使用 PGO 優化。


[Profile-guided optimization (PGO)]:https://en.wikipedia.org/wiki/Profile-guided_optimization