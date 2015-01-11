---
layout: post
title: "linux kernel 安裝 aufs "
date: 2014-12-26 23:18:05 +0800
comments: true
categories: ["linux"]
---

<!-- more -->


之前研究 Docker 了解了有一個 aufs 檔案系統，所以就想安裝來玩玩看。

#### 概要
我是用手上的 Centos 6 測試的，安裝前要先下載下面幾個檔案，然後使用 `aufs3-standalone` 給
aufs3-linux 打上補丁然後在 config 時打開 aufs 的選項後編譯核心即可。

1. aufs3-linux 
2. aufs3-standalone 
3. aufs-util git://git.code.sf.net/p/aufs/aufs-util

#### 下載

	git clone git://github.com/sfjro/aufs3-linux.git
	git clone git://git.code.sf.net/p/aufs/aufs-util
	cd aufs3-linux
	git clone git://git.code.sf.net/p/aufs/aufs3-standalone

#### 切換版本
切換 `aufs3-linux` 和 `aufs3-standalone` 的版本，目前支援到最新的 3.18 版本，
但是要注意兩個版本要一致。

#### 打上補丁 

	aufs3-standalone/aufs3-kbuild.patch
	aufs3-standalone/aufs3-base.patch
	aufs3-standalone/aufs3-mmap.patch
	aufs3-standalone/aufs3-standalone.patch

#### 從aufs3-standalone 複製必要的檔案到 kernel
	{Documentation,fs}
	include/linux/aufs_type.h 
	include/uapi/linux/aufs_type.h

#### 最後
打開 aufs 的編譯選項，然後編譯核心重開機後還需要安裝 `aufs-util`，這樣 aufs 才能正常運作。
