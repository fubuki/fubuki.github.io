---
layout: post
title: "mitmproxy 安裝和使用"
date: 2015-08-05 22:52:01 +0800
comments: true
categories: [""]
---


<!-- more -->

之前開發給手機的 API 都是直接看 `server log`，然而最近看到有個專案 [mitmproxy] 可以使用看看，可以直接做為代理
記錄 client 的呼叫，之前有想在 apache 上裝套件方便監視所有 API 的呼叫和傳輸資料，不過現在有這個就不需要了，另外
也可以自行撰寫指令搞擴充想要的功能。

### 安裝
直接用 pipe 安裝就好

	pip install mitmproxy



[mitmproxy]:https://github.com/mitmproxy/mitmproxy