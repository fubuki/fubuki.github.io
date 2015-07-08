---
layout: post
title: "memcache connect vs pconnect"
date: 2014-05-23 21:31:20 +0800
comments: true
categories: ["memcached"]
---

memcached 目前算是常用的快取server，很多人在使用php開發網站通常會搭配memcached，本文記錄一下
php 在使用 memcache library 遇到的問題。

<!-- more -->

memcache 有分 connect 和 pconnect 兩種方法，但是 connect 會斷掉連線，而 pconnect 會將連接持久化，從curr_connections可以看出
兩者的不同，同一個網頁重整 conncet 的 curr_connections 數值不會一直增加，但是 pconnet 會上升到一個上限。

但是在網路上有看到人說 fastcgi方式用長連接是無效的，這邊還需要了解關於pconnect是如何實作的，似乎是用 zend_list_insert 實作的。