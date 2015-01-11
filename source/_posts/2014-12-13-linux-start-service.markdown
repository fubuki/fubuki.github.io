---
layout: post
title: "管理 linux 啟動執行的服務"
date: 2014-12-13 23:09:26 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

在 Liinux 使用 `update--rc.d` 或是 `chkconfig` 管理開機時要啟動哪些服務，兩者用法是類似的，
另外還有 Ubuntu 底下也有 `rcconf` 和 `sysv-rc-conf` 可以使用，不過上面的指令會提到關於執行 level 的概念
決定服務要在哪個時候執行。

