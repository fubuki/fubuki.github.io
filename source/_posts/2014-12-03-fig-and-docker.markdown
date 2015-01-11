---
layout: post
title: "使用 fig "
date: 2014-12-03 23:05:08 +0800
comments: true
categories: ["docker"]
---


<!-- more -->

[fig] 是一個跟 docker 有關的命令列管理工具，看起來比 coreos 本身簡單許多適合初學者使用但是提供功能就比較少，
不過在網路上看到有人有些轉換工具可以將 fig 產生的設定轉換成 coreos 所需的格式，所以可以先玩玩 fig 覺得不錯在
轉用 coreos。


下面官網在 ubuntu 下的安裝方法

	curl -L https://github.com/docker/fig/releases/download/1.0.1/fig-`uname -s`-`
	uname -m` > /usr/local/bin/fig; chmod +x /usr/local/bin/fig

[fig]:http://www.fig.sh/