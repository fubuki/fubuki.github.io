---
layout: post
title: "phalcon 設定讀寫分離功能"
date: 2015-04-02 23:29:18 +0800
comments: true
categories: ["php"]
---

<!-- more -->

最近需要建立 phalcon 連結 mysql 的專案，然後手上有一個 mysql cluster 的設備，所以
想要在 phalcon 設定讀寫分離的功能，讀跟寫是連接不同的資料庫位置，最後在 phalcon 的文檔
[setting-multiple-databases] 有說明怎麼設定。



[setting-multiple-databases]:https://phalcon-php-framework-documentation.readthedocs.org/en/latest/reference/models.html?highlight=selectReadConnection#setting-multiple-databases
