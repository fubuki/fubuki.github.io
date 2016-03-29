---
layout: post
title: "Covering Index"
date: 2016-02-29 23:40:00 +0800
comments: true
categories: ["database"]
---


<!-- more -->

使用 `Covering Index` 優化查詢速度，主要是在輸出 column 時只選擇有索引的 column，
不過這跟資料庫底層怎麼搜尋資料以及索引跟資料的存放方式有關。