---
layout: post
title: "Phalcon Dynamic Update DataBase"
date: 2015-04-15 23:12:10 +0800
comments: true
categories: ["php"]
---

<!-- more -->

Phalcon 在更新資料庫的資料時會將所有欄位的資料都更新上去無論是有沒有修改過 Model 的欄位，這樣在某些情況下會有問題，
如果使用 oracle 的 clob 欄位時必須先取得 stream 的內容後在更新，不然會發現資料內容都變成 resource id。

不過後來發現 Phalcon 的 [Dynamic Update]  功能可以避免上述的問題，使用這個功能後 phalcon 在產生 sql query 時只會更新
 Model 有修改的部分。

[Dynamic Update]:http://docs.phalconphp.com/en/latest/reference/models.html#dynamic-update