---
layout: post
title: "Linux taskset 指令"
date: 2015-01-17 23:20:43 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

Linux 有個 taskset 指令可以在多核環境下指定特定的 Process 在某個 CPU 下運行，這個指令是看到有人用在 node.js 腳本上，
由於 node.js 本身如果沒有特別處理是無法發揮多核的效能，所以建立多個 node.js Process 然後個別指定每個 CPU 上面，這樣
就可以將使用到多核的效能。


