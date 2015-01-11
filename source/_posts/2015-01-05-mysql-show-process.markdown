---
layout: post
title: "Mysql 顯示進程列表"
date: 2015-01-05 22:12:57 +0800
comments: true
categories: ["mysql"]
---


<!-- more -->

檢查目前 mysql 有多少進程，並且可以看出有多少連線，目前有在跑哪些 sql 和執行了多久，
有時網站變慢可以從列表中觀察是哪些 sql 拖慢系統的速度，另外也可以透過 kill 直接殺掉進程。

	show processlist;
	show full processlist;
	kill
