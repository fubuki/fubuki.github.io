---
layout: post
title: "使用 strace 跟蹤進程"
date: 2015-01-08 23:28:43 +0800
comments: true
categories: ["linux"]
---


<!-- more -->

之前使用 lighttpd + web.py 架設環境時不知道什麼原因跑不起來，但是 log 裡面沒有顯示可用的訊息除錯，
後來學到使用 `strace` 追蹤 lighttpd 的運行過程，查到是有模組沒有安裝造成的。

直接運行

	strace -ff lighttpd -D -f /etc/lighttpd/lighttpd.conf

透過 pid 跟蹤
	

透過 port 跟蹤