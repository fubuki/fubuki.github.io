---
layout: post
title: "針對短文本做語言偵測"
date: 2015-08-13 21:08:49 +0800
comments: true
categories: ["nlp"]
---


<!-- more -->


針對類似 `tweet` 的短文本進行語言偵測。以前有用過 Tika 實做語言偵測不過命中率從別人的測試數據看起來不太好，
之後從別的地方聽到了 [cld2] 效果會比較好，不過在對很文本長度不長情形下準度會下降，所以另外研究了 [Short Text Language Detection with Infinity-Gram]
使用其他方法嘗試解決這類的問題。


[cld2]:https://github.com/CLD2Owners/cld2
[Short Text Language Detection with Infinity-Gram]:http://www.slideshare.net/shuyo/short-text-language-detection-with-infinitygram-12949447
[Language Detection Library for Java]:http://www.slideshare.net/shuyo/language-detection-library-for-java