---
layout: post
title: "Yum 出現 Cannot retrieve metalink for repository: epel 的錯誤"
date: 2014-12-30 22:49:21 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

在 Centos 6 上面更新套件的時候出現了 `Cannot retrieve metalink for repository: epel` 的錯誤，
命令列是寫說是因為 SSL 連線出問題，後來從網路上看到是要更新 [nss] 這個套件。


[nss] 全名是 `Network Security Services` 似乎是負責網路加密傳送的功能，不知道是版本的關係才會出現
 SSL 問題，在網路上也到有一些加密的問題也是出自於 [nss]，而在 MDN 也有一篇 [Overview of NSS] 的文章，
 裡面也說明 nss 是一個開源的加密函式庫，而 Yum 有使用到 nss 處理 SSL 加密連線。







[nss]:http://en.wikipedia.org/wiki/Network_Security_Services
[Overview of NSS]:https://developer.mozilla.org/en-US/docs/Mozilla/Projects/NSS/Overview