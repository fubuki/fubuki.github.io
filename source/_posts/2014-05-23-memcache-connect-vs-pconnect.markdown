---
layout: post
title: "memcached connect vs pconnect"
date: 2014-05-23 21:31:20 +0800
comments: true
categories: ["php"]
---

memcache目前算是常用的快取server，很多人在使用php開發網站通常會搭配memcached，本文記錄一下
php 在使用memcached遇到的問題。
<!-- more -->

memcached 有分 connect 和 pconnect兩種方法，但是connect會斷掉連線，而pconnect會將連接持久化，從curr_connections可以看出
兩者的不同，同一個網頁重整conncet的curr_connections數值不會一直增加，但是pconnet會上升到一個上限。

但是在網路上有看到人說 fastcgi方式用長連接是無效的，這邊還需要了解關於pconnect是如何實作的。