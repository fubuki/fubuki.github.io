---
layout: post
title: "MySQL 分區表"
date: 2014-06-15 23:49:06 +0800
comments: true
categories: ["mysql"]
---

記錄一下在MySQL下 分區表的種類和用法。

<!-- more -->


##種類
1. RANGE分區
2. LIST分區
3. HASH分區
4. KEY分區
5. COLUMNS分區


##用法
1. 子分區
2. 根據日期作RANGE分區優化查詢速度
3. LIST分區用於不連續離散的數值
4. HASH和KEY用來均勻的分配數據到各個分區
5. COLUMNS用在非整數類型的數值欄位
