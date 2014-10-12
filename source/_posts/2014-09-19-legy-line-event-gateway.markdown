---
layout: post
title: "LEGY (LINE Event Gateway)"
date: 2014-09-19 23:44:34 +0800
comments: true
categories: ["LINE"]
---

<!-- more -->

之前有機會看到 LINE　的整個架構圖的時候看到一個 LEGY 的區塊，看起來是負責跟 Client 端連結的部分，並且所有的平台都是透過 LEGY 跟後端程式連結，
之後在 Line 的開發者大會跟一些 twitter上的訊息得知 LEGY (LINE Event Gateway) 使用 erlang 撰寫的組件，負責分發前端傳來的請求，據說之後會在 LINE Engineers' Blog 有
更詳盡的介紹。