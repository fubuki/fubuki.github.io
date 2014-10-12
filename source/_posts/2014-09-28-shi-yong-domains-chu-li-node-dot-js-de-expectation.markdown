---
layout: post
title: "使用 domains 處理 node.js 的 expectation"
date: 2014-09-28 22:47:23 +0800
comments: true
categories: ["nodejs"]
---

<!-- more -->

寫 node.js 久了之後程式會慢慢變大因此有時會出現 `uncaughtException` 的問題，由於 node.js 異步的特性所以會無法抓取到錯誤並處理它，
所以在 node.js 0.8 之後出現了 domains 的模組讓開發者使用。


	var domain = require('domain');
	var d = domain.create();
	var serverDomain = domain.create();
	serverDomain.run(function() {


	});