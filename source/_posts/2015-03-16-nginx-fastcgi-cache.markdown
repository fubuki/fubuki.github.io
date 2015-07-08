---
layout: post
title: "nginx 的 fastcgi_cache 模組"
date: 2015-03-16 22:44:09 +0800
comments: true
categories: ["nginx"]
---

<!-- more -->

在看 [[Golang] Go言語でサービス作ってる話] 這篇投影片的時候看到了一個東西 [fastcgi_cache]， 在 fastcgi 層加上 cache，
不過要如何決定哪些要快取，還需要研究這邊有兩篇很有趣的文章可以參考 。

1. [通过FastCGI Cache实现服务降级] 
2. [Nginx模块fastcgi_cache的几个注意点]




[fastcgi_cache]:http://wiki.nginx.org/HttpFastcgiModule
[[Golang] Go言語でサービス作ってる話]:http://www.slideshare.net/yoshikazuhashimoto/go-37911621
[通过FastCGI Cache实现服务降级]:http://huoding.com/2014/01/13/321
[Nginx模块fastcgi_cache的几个注意点]:http://www.cnxct.com/several-reminder-in-nginx-fastcgi_cache-and-php-session_cache_limiter/