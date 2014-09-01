---
layout: post
title: "boosting and bagging"
date: 2014-08-08 23:28:16 +0800
comments: true
categories: ["algorithm"]
---

<!-- more -->
Ensemble learning (集成學習)，似乎是混合多個學習演算法提高結果的精確度 ，而 boosting 和 bagging便是
其中集成學習的兩種方法，下面整理一些學習資源。


### boosting

AdaBoost（Adaptive Boosting） 

使用同一個訓練集， 每次訓練的時候針對有問題訓練資料加大權重，讓函數靠往有問題的訊息資料。


### bagging

每次訓練函數的時候從資料取出子資料集，然後多次訓練函數，最後有多個分類函數以投票方式分類新的資料。



### 差別