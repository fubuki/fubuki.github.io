---
layout: post
title: "memcached with namespace"
date: 2014-06-24 21:23:07 +0800
comments: true
categories: ["memcached"]
---

memcached如何實作namespace的方法。

<!-- more -->


memcached沒有支援namespace所以沒辦法直接批量刪除鍵值，原本是可以直接拉出在memcached裡面的key然後只
刪除想要刪除的鍵值，但是從取出所有key會很耗費資源所以不會考慮，之後有想過在DataBase的地方存放所有
key然後就可以快速查詢想要批量刪除的鍵值，最後是使用Deleting by Namespace的方法，實作出namespace後
透過namespace批量刪除，實作可以參考[NewProgrammingTricks]，其實他的主要想法是使用固定的key pattern
實作namespace，在透過管理namespace的版本號讓舊的cache自然失效。



[NewProgrammingTricks]:https://code.google.com/p/memcached/wiki/NewProgrammingTricks#Namespacing