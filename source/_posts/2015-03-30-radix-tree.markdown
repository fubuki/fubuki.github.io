---
layout: post
title: "radix tree"
date: 2015-03-30 22:03:10 +0800
comments: true
categories: [""]
---

<!-- more -->

最近在看 nginx 和紅黑樹時看到一種名叫 `radix tree` 的多元搜尋樹，後來了解到在 linux 使用 `radix tree` 管理 cache，
linux 裡面相關的程式碼在 [radix-tree.c] 裡面。


[radix-tree.c]:https://github.com/torvalds/linux/blob/master/lib/radix-tree.c