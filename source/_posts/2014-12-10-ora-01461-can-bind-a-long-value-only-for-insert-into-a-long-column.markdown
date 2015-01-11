---
layout: post
title: "ORA-01461: can bind a LONG value only for insert into a LONG column"
date: 2014-12-10 22:51:27 +0800
comments: true
categories: ["php"]
---

<!-- more -->


今天在工作上遇到了 "ORA-01461: can bind a LONG value only for insert into a LONG column" 這個錯誤訊息，後來發現是
因為有人在資料庫使用 `clob` 的關係，似乎是插入的字串超過了 4k 的長度。

之前使用 `clob` 時應該是支援超過 4k 長度的字串，網路上找了一些大部分都是寫 JDBC 版本的問題，不過我們開發環境是 PHP，
原本以為是 oracle client 版本跟資料庫不一樣導致的問題，不過兩者版本是一致的，後來用 `oci_bind_by_name` 就可以過去了，
而在 phalcon 底下使用 phql bind param 的方式也能夠執行避免錯誤，似乎問題在於 phalcon 使用 pdo 實現 oracle 的問題，
直接使用 model 賦值是無法成功寫入的。
