---
layout: post
title: "MLDM Monday --- 中文搜尋經驗分享 "
date: 2015-09-14 23:26:59 +0800
comments: true
categories: ["elasticsearch"]
---

<!-- more -->

今天去參加一場 Meetup 內容是 [中文搜尋經驗分享]，主要是講 Pinkoi 怎麼使用 elasticsearch 建立電商搜尋服務。

內容是先簡介一下 elasticearch 然後解說怎麼使用  jieba ，並且使用一些繁體中文資源建立 jieba 分詞用的詞典，
這邊是使用 wikipedia 和萌典，不過由於 jieba 是中國大陸那邊開發的所以有些訓練出來的模型像是 HMM 是針對簡體中文，
需要另外重新訓練或是處理。

最後就是介紹 word2vec，使用斷詞過的 wikipedia + gensim 建立資料，這是為了處理使用者搜尋不到的情形，找尋相關的關鍵字。


[中文搜尋經驗分享]:http://blog.liang2.tw/2015Talk-Chinese-Search/#cover