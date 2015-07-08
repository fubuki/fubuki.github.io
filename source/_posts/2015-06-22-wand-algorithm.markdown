---
layout: post
title: "wand algorithm"
date: 2015-06-22 22:25:31 +0800
comments: true
categories: ["algorithm"]
---


<!-- more -->

之前在研究 ssdeep 演算法時另外看到的跟倒排有關的演算法，名為 wand (weak and)，這裡有一篇相關的論文 `Efficient Query Evaluation using a Two-Level Retrieval
Process` ，使用 wand 在搜尋引擎上可以增加搜尋的速度，先用速度較快的但是模糊較不精準的演算法過濾後，在使用耗時但是精準的演算法對文檔做排序。