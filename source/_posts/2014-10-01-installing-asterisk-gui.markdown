---
layout: post
title: "安裝 Asterisk GUI"
date: 2014-10-01 23:30:42 +0800
comments: true
categories: ["asterisk"]
---

<!-- more -->


最近裝完 Ansterisk 後需要一個方便的 web 介面管理，在網路上找了一下就先使用了看起來很簡單的 `Asterisk GUI`。


#### 安裝
可以使用 yum 或是直接下載源碼安裝，我是直接使用 yum安裝。
	
	yum install asterisk-gui

#### 設定 
需要設定 `http.conf` 和 `manager.conf` 這兩個檔案，這兩個檔案都在 `/etc/asterisk/` 底下，設定檔裡面都有簡單的說明，只要參照裡面的說明開啟選項即可，但是如果使用 yum 安裝似乎會有問題需要設定軟連結才能正確的開啟 Asterisk GUI。

	ls /var/lib/asterisk/static-http/config && rm -rf /usr/share/asterisk/static-http && ln -s /var/lib/asterisk/static-http /usr/share/asterisk/static-http