---
layout: post
title: "android webview 的 坑"
date: 2015-04-20 22:59:45 +0800
comments: true
categories: ["android"]
---


<!-- more -->

### 解決 Android ViewPort 失效的問題

	webView.getSettings().setLoadWithOverviewMode( true );
	webView.getSettings().setUseWideViewPort( true );



### samsung 的手機頁面中有 Canvas 使用 touch 事件會有 bug

	z-index 的 BUG。


### windows.outterWidth 為零的問題