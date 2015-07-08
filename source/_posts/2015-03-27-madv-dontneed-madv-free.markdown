---
layout: post
title: "MADV_DONTNEED 和 MADV_FREE"
date: 2015-03-27 03:05:32 +0800
comments: true
categories: ["linux"]
---


<!-- more -->

在看 firefox 記憶體管理的程式碼時看到下面兩個名詞。

1. MADV_DONTNEED 會馬上回收指定的記憶體區塊
2. MADV_FREE kernel 會延遲回收那些頁面