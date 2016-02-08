---
layout: post
title: "使用 stream2es 匯入 Wikipedia 資料"
date: 2015-09-05 23:38:48 +0800
comments: true
categories: ["elasticsearch"]
---


<!-- more -->


目前手上已經有一些 Wikipedia 的資料，這是之前在使用 nlp4l 做為輸入資料遺留下來的，
那時使用了 json-wikipedia 將 xml 轉換成 json ，使用 jq 看過一遍大致上了解了內容的
資料結構，不過由於資料太過於龐大搜尋起來很久，所以使用了之前看到的工具 stream2es 將
手上的資料轉換到 elasticsearch 裡面。


最後轉換的結果有點少，只有一百九十萬多筆，有些資料似乎沒有匯入進去，之後要換用 Logstash
 匯入應該會有不一樣的結果。