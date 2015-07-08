---
layout: post
title: "android remote debug"
date: 2015-04-21 21:33:13 +0800
comments: true
categories: ["android"]
---

<!-- more -->


最近在 Android 上開發 `Hybrid app` 遇到一些問題，裡面有些頁面在設計的時候使用了很多外部的套件導致 layout 跟預計的
相差很大，並且撰寫 javacript 的工程師使用的一些語法在桌面瀏覽器是可以但是在 webview 內是不行的，這樣產生了不少問題
並且很難除錯，後來參考了一篇 [Remote Debugging on Android with Chrome]，讓開發者可以藉由 usb 和 chrome 遠端除錯。

### 開啟 chrome 遠端除錯的功能

	chrome://inspect/

### 在 webview 增加下列程式碼

	if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
		WebView.setWebContentsDebuggingEnabled(true);	
	}

[Remote Debugging on Android with Chrome]:https://developer.chrome.com/devtools/docs/remote-debugging