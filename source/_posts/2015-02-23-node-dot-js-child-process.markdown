---
layout: post
title: "node.js 建立 child process"
date: 2015-02-23 22:49:18 +0800
comments: true
categories: ["nodejs"]
---

<!-- more -->

最近在測試將手上一個 node.js 的系統分成好幾個子系統，然後主要的系統就只是去監控子系統
避免當子系統出現問題時導致整個系統出現問題，這邊紀錄一下 node.js 怎麼建立 child process。


以前有用過 node.js 的 cluster 模組去擴展 socket.io 的伺服器，現在是用 `child process` 模組建立
新的 process 收到處理完成的訊息後就將 process 給殺掉， `child process` 目前有提供下面幾種方法。


1. spawn
2. exec
3. execFile
4. fork