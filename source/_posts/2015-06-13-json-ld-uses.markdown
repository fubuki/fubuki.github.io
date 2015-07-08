---
layout: post
title: "JSON-LD  用途"
date: 2015-06-13 23:04:58 +0800
comments: true
categories: [""]
---

<!-- more -->

JSON-LD 是為了增強 JSON 而設計出來的，原本 JSON 只是單純的 key-value 的存放格式，光從 JSON 的資料上式無法準確
得知這個欄位代表的意思，然而藉由 JSON-LD 可以原本單純的資料讓帶有意義。


## 用途

### Search Engine
原本像是 Google ,Yahoo 之類的搜尋引擎在抓取網站內容時，根據包裹資料的標籤可以了解資料的重要程度，卻無法了解資料代表的意義，
然而透過類似 JSON-LD 的 MicroData可以讓搜尋引擎更能讓使用者找到想要的情報。


### Web Api
一些提供 Restful API 的 web service，如果透過使用 JSON-LD 便可以讓接收端更有效的處理資料內容，
也許透過抽換 JSON-LD 的內容就可以改變資料處理方式。 


### Data Store

Web Components + JSON-LD。
