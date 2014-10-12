---
layout: post
title: "PHPCI 安裝過程"
date: 2014-08-02 23:49:24 +0800
comments: true
categories: ["php","continuous integration"]
---

<!-- more -->

[phpci] 看起來是專門為 PHP 持續集成所做的， 這是他的[github]， 它的wiki有寫怎麼安裝，
不過裝不起來所以在這邊記錄一下安裝過程。

我這邊是先從 github clone 一份下來，然後我資料庫使用 MariaDB ，server 使用 nginx，
然後使用 composer 安裝必要的部分，但是它本身所以用的 framework 有bug 還要更新，但是
還是有相同的錯誤出現。



[PHPCI]: https://www.phptesting.org/
[github]:https://github.com/Block8/PHPCI