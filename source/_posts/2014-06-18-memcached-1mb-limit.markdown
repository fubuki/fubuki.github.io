---
layout: post
title: "memcached 1MB limit"
date: 2014-06-18 23:06:14 +0800
comments: true
categories: ["memcached"]
---

memcached在儲存單筆記錄的時候會有個限制，每筆記錄只能存放最大1MB的大小，以前沒有遇過這種問題，但是在最近一個
專案上面突然遇到快取沒有作用的問題，後來發現有可能是存放的資料大於1MB的問題，在[ha-memcached-faq]裡面有說為什麼
預設1MB和如何調整大小。


[ha-memcached-faq]:http://docs.oracle.com/cd/E17952_01/refman-5.6-en/ha-memcached-faq.html
