---
layout: post
title: "PHP  的 pcntl_fork 函式"
date: 2015-08-20 23:18:11 +0800
comments: true
categories: ["php"]
---

<!-- more -->

最近在使用 PHP 撰寫 CLI 的功能時，想要實做能夠根據 CPU 數量自動 auto scale 加快計算的功能，
所以在尋找 PHP 裡面跟 fork 有關的函式，最後找到了 pcntl_fork 這個函式能夠 fork 出多個 process ，
使用上不太難不過子進程結束需要自行。