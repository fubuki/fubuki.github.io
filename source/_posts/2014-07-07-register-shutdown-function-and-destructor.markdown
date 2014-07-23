---
layout: post
title: "auto restart php script by register_shutdown_function and pcntl_exec"
date: 2014-07-07 23:07:53 +0800
comments: true
categories: ["php"]
---

在使用PHP CLI 跑背景程式有時候會因為記憶體溢出或是其他原因導致程式停止執行，需要讓程式自行重新啟動。

<!-- more -->

register_shutdown_function 是可以讓PHP在意外終止的時候可以去執行特定函式，配合 `pcntl_exec()` 便可以
完成當程式發生FatalError 時可以自動重新啟動。


<script src="https://gist.github.com/fubuki/e621eb4844a975b9c0e1.js"></script>


