---
layout: post
title: "PHP 之 fastcgi_finish_request"
date: 2014-06-29 23:02:40 +0800
comments: true
categories: ["php"]
---

PHP 在 fast-cgi 模式下有一個有趣的函式 `fastcgi_finish_request` 可以使用，在[function.fastcgi-finish-request]
有說明這個函式是讓開發者強制停止與客戶端之間的連線，但是服務端的腳本還是持續執行，這讓客戶端可以不用等待一些耗時的操作，
不過如果要達成類似的效果我還是比較喜歡用丟到隊列去執行的方法。



[function.fastcgi-finish-request]:http://php.net/manual/en/function.fastcgi-finish-request.php