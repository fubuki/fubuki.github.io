---
layout: post
title: "圖片搜尋的演算法"
date: 2015-08-01 23:42:19 +0800
comments: true
categories: ["algorithm"]
---

<!-- more -->


之前有在找 google 以及其他網站的以圖找圖服務是怎麼做的，以前想過應該是用 hash 的方式比對會比較快，
不過不知道是用怎麼樣的 hash 演算法，然後最近看到了 [Perceptual hashing]，似乎可以用來做圖片搜尋的演算法，
不過不知道精準度如何，另外還有 [SIFT] 取出特徵點進行分析以及另外一種 [pHash] 的算法。



[Perceptual hashing]:https://en.wikipedia.org/wiki/Perceptual_hashing
[pHash]:http://www.phash.org/
[SIFT]:https://en.wikipedia.org/wiki/Scale-invariant_feature_transform