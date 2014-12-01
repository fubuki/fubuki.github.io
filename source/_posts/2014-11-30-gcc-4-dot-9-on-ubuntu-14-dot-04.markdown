---
layout: post
title: "在 Ubuntu 14.04 快速安裝 gcc-4.9"
date: 2014-11-30 19:45:48 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

最近將作業系統從 Ubuntu 12.04 LTS 升級到 14.04 LTS ，裡面的軟體也一併升級但是後來發現 gcc 只有到 `4.8` 的版本，沒有到最新的
 `4.9` 版本，沒有辦法完整支持 `C++ 14` 的標準。

原本要使用源碼直接編譯，但是發現在 Ubuntu 可以透過 apt 安裝 `g++ 4.9` ，下面記錄透過 apt 安裝的指令。

	sudo add-apt-repository ppa:ubuntu-toolchain-r/test
	sudo apt-get update
	sudo apt-get install g++-4.9
	gcc-4.9 -v
