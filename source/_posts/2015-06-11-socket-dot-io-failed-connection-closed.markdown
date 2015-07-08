---
layout: post
title: "socket.io failed: Connection closed"
date: 2015-06-11 22:35:48 +0800
comments: true
categories: ["socketio"]
---

<!-- more -->

今天在使用新版的 Socket.io 的時候遇到了一個問題，當我使用 mulit-node 的模式時，在瀏覽器的控制台會出現下面這段錯誤，

	failed: Connection closed before receiving a handshake response

後來在 socket.io 的 github 也有看到人 po 出相同的 issue，之後看了 issue 下面的回應似乎是 Sticky Session 的問題，但是我
是在同一台機器上使用 cluster 模組 fork 出多個子進程，這樣 Sticky Session 是否有用還需要研究和測試。