---
layout: post
title: "偵測 android 的 APP 是否被移除了"
date: 2014-08-22 23:54:59 +0800
comments: true
categories: ["android"]
---

<!-- more -->

日前被要求能不能找出有多少人移除我們開發的 APP，關於這個問題似乎在 google play 的後台好像有
顯示多少人移除 APP，不過沒辦法得知有有哪些人移除，後來在對 GCM 除錯的時候有的人會回傳 `not registered`
的錯誤訊息，查詢代表的意義是使用者移除的 APP，便可以透過這個方法得知。