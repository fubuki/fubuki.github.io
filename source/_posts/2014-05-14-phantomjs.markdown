---
layout: post
title: "phantomjs"
date: 2014-05-14 21:19:15 +0800
comments: true
categories: ["javascript"]
---

[phantomjs] 是類似nodejs的工具，都是使用javascript驅動，不過nodejs是使用v8引擎而phatomjs是使用webkit，
而webkit裡面除了js引擎的部分也有包含html渲染的部分，也因此phantomjs能夠生成html的頁面，就像是一個閱覽器。


目前在專案上我最常使用phantomjs於頁面截圖和前端js測試，可以利用phantomjs取得某個網址的頁面然後保存下來，
然後可以製作一個書籤服務並且加上網站截圖或是預覽圖的功能，phantomjs可以和Selenium針對前端作單元測試。

一篇關於webkit的參考資料:[webkit-for-developers]


[phantomjs]: http://phantomjs.org/
[webkit-for-developers]: http://www.paulirish.com/2013/webkit-for-developers/