---
layout: post
title: "freeswitch 動態更改 sip 使用者資訊"
date: 2014-10-21 22:29:29 +0800
comments: true
categories: ["sip"]
---

<!-- more -->

freeswitch 預設是透過將 sip 使用者資訊寫入一份 xml 檔案，不過可以透過一些方法動態增加使用者資訊，
目前可以透過 `xml_curl` 這個模塊將 freeswitch 一些行為使用 curl 的方式跟外部 server 連接認證使用者資料。


#### 安裝 xml_curl

下載 http://files.freeswitch.org/ 的 freeswtich 原始碼，編輯 module.conf 將 xml_curl 的註解去除。   

	./configure  
	make mod_xml_curl-install

#### 載入 xml_curl
編輯 `/etc/freeswitch/autoload_configs` 重啟 freeswitch。  
也是可以使用 fs_cli Mod commands 載入模組。   
編輯 xml_curl.conf.xml 讓 freeswitch 要怎麼跟後端的 web service 溝通。 

#### 設定 Freeswitch-Contrib
下載 [Freeswitch-Contrib]，在 `intralanman/PHP/fs_curl` 底下的程式碼放到可以執行 PHP 的伺服器，
設定要使用哪種資料庫，伺服器上面要安裝 PDO 讓 PHP 可以跟資料庫連結。

[Freeswitch-Contrib]:https://freeswitch.org/stash/projects/FS/repos/freeswitch-contrib/browse

#### 動態增加使用者資料
最後更改資料庫的資料測試效果。
