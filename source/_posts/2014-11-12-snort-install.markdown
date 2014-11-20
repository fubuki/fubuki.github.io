---
layout: post
title: "如何安裝 snort"
date: 2014-11-12 21:26:49 +0800
comments: true
categories: ["snort"]
---


<!-- more -->

[snort] 是一個入侵偵測系統，在網路上有一些現成的規則檔載入到 snort，也可以自行撰寫需要的規則。


###下載 snort 和 daq。

	wget https://www.snort.org/downloads/snort/daq-2.0.4.tar.gz
	wget https://www.snort.org/downloads/snort/snort-2.9.7.0.tar.gz

###安裝 libdnet
在 ubuntu 底下安裝時會發現需要比較新的 [libdnet] 版本，使用 [checkinstall] 建立 deb 檔後安裝。  


### 安裝 daq 和 snort



### 下載官方 RULE

	wget https://www.snort.org/rules/community
	tar -xvfz community.tar.gz -C /etc/snort/rules

[snort]:https://www.snort.org/
[libdnet]:https://code.google.com/p/libdnet/
[checkinstall]:http://www.ibm.com/developerworks/cn/linux/l-cn-checkinstall/