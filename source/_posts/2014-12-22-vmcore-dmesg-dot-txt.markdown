---
layout: post
title: "分析 vmcore 和 vmcore-dmesg.txt"
date: 2014-12-22 23:11:07 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

今天在試玩 docker 的時候，因為不知名因素導致系統直接重啟，後來發現是整個內核 crash 原因是似乎是跟 `device-mapper` 脫不了關係，
看他 console 列出的最後訊息可以得知在 `/var/crash` 生成了兩個文件: `vmcore` 和 `vmcore-dmesg.txt`。


在 `/var/crash` 下面的兩個文件是記錄了系統 Crash 時的最後訊息，可以透過這些文件追蹤發生了什麼事，要追蹤需要使用幾個工具: kdump 和 crash 
，kdump 是讓系統 Crash 時將內核的訊息 dump 到硬碟上以供使用者除錯， crash 是可以去分析 `vmcore` 的內容，但是需要 vmlinux 的檔案才能分析
 vmcore 的內容， vmlinux 需要跟目前的系統核心相同。


 另外一個 vmcore-dmesg.txt 檔案是記錄一些系統資訊和 Crash 時的資訊，雖然沒有比 vmcore 詳細但是也可以作為參考，