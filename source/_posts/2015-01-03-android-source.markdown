---
layout: post
title: "取得 Android 的原始碼"
date: 2015-01-03 22:20:12 +0800
comments: true
categories: ["android"]
---

<!-- more -->



1. 安裝 repo

	curl https://storage.googleapis.com/git-repo-downloads/repo > /usr/bin/repo
	chmod  a+x /usr/bin/repo

2. 建立文件夾下載程式碼

	mkdir andorid_source
	cd andorid_source
	repo init -u https://android.googlesource.com/platform/manifest
	repo sync


參考 : [Downloading the Source]

[Downloading the Source]:https://source.android.com/source/downloading.html