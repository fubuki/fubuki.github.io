---
layout: post
title: "Centos 6 升級核心到 3.18"
date: 2014-12-25 01:21:48 +0800
comments: true
categories: ["linux"]
---


<!-- more -->


今天把手上的 Centos 的核心從 2.6 升級到 3.18，順便紀錄一下升級的過程。

先下載新版的 Linux Kernel 檔案並且解壓縮。

	wget  https://www.kernel.org/pub/linux/kernel/v3.x/linux-3.18.1.tar.gz
	tar zxf linux-3.18.1.tar.gz

設定編譯選項，我原本找不到舊的編譯檔案，後來在 `/usr/src/kernel` 底下找到。

	cp /usr/src/kernel/config .config
	make menuconfig

開始編譯核心和模組，加上 -j 參數使用多核心編譯。

	make -j bzImage 
	make -j modules 
	make -j modules_install 


安裝並且修正開機順序後重開機。

	make install
	vim /etc/grub.conf
	reboot


重開機後就可以看到核心已經變成 3.18 版本，不過卻出現另外一個問題，當我要使用 `docker` 
的時候卻出現 iptables 的錯誤，最後發現是編譯的時候沒有將 NAT 的模組編譯進去所導致的問題，
之後重新編譯就可以了。
	

