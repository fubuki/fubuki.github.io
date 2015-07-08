---
layout: post
title: "使用 URL 對網頁做分類"
date: 2015-05-28 21:10:40 +0800
comments: true
categories: [""]
---

<!-- more -->


[URL-based Web-Page Classification] 使用 N-gram 資料做訓練集， LingPipe 做為 NLP 的函式庫，
LM Classifier 使用 Naive Bayes 做分類，對於未見過的字串使用 Laplace smoothing 補足。

也有提到下面幾種分類方法:

    1. Naive Bayes
    2. SVM
    3. Maximum Entropy
    4. Online Learners



[URL-based Web-Page Classification]:https://tarekamr.appspot.com/msc/presentation