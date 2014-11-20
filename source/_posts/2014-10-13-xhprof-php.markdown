---
layout: post
title: "使用 xhprof 測量 php 函式效能"
date: 2014-10-13 23:45:28 +0800
comments: true
categories: ["php"]
---

<!-- more -->

之前有在尋找一些關於 PHP 除錯用的工具意外看到 [xhprof]，似乎可以測量 PHP function 層級的效能，之前在測試專案效能
通常是透過 ab 去測試併發數，並沒有基於單一函式進行測試，透過這個工具應該更容易找出問題在哪，這邊有個[教學]可以參考。

[xhprof]:https://github.com/phacility/xhprof
[教學]:https://blog.engineyard.com/collections/profiling-with-xhprof-and-xhgui/