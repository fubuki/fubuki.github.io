---
layout: post
title: "nginx use sticky session by cookie"
date: 2015-04-30 00:42:38 +0800
comments: true
categories: ["nginx"]
---



<!-- more -->

使用 nginx 作 proxy 的時候有時會希望相同的客戶端連線都會連結到相同的機器，因為有可能每台機器各自存放著一些資料，
而那些資料是沒有共享的，如果客戶端連到另外的主機就會遺失一些資料。

例如我每台機器都有各自 memcached 用來存放一些快取資料，如果客戶端沒有連線到相同主機便會失去這些快取資訊。


要在 nginx 上使用 sticky seession 需要安裝  [nginx-sticky-module-ng]，安裝之後就可以在設定檔中使用 `sticky` ，但是
這個功能是使用 cookie 完成的，所以如果 cookie 有問題就會需要使用 `ip-hash` 代替。


[nginx-sticky-module-ng]:https://bitbucket.org/nginx-goodies/nginx-sticky-module-ng/overview