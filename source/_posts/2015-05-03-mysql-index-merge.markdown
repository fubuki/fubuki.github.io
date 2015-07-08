---
layout: post
title: "MySQL 的 Index Merge Optimization"
date: 2015-05-03 21:27:45 +0800
comments: true
categories: ["mysql"]
---


<!-- more -->


在 MySQL 中如果在一個表中有多個 Index 然後 SQL 語句使用到這些 Index ， MySQL 就
會使用 [Index Merge Optimization] 。




[Index Merge Optimization]:http://dev.mysql.com/doc/refman/5.0/en/index-merge-optimization.html