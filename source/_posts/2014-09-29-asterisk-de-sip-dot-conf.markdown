---
layout: post
title: "Asterisk 的 sip.conf"
date: 2014-09-29 23:28:49 +0800
comments: true
categories: ["asterisk"]
---

<!-- more -->

Astreisk 的 sip 設定位於 `/etc/asterisk/sip.conf`，設定完後使用 softphone 進行測試，另外 LINE 的 VoIP 是使用 sip 和 rtp 構成的。
參考[Asterisk基本設定ガイド]裡面的文章

### 設定檔

[general]  
context=default  
port=5060  
bindaddr=0.0.0.0  
srvlookup=yes  
disallow=all  
allow=ulaw  
allow=alaw  
allow=gsm  
language=zh-tw 

[201]  
type=friend  
類型有 peer user friend  
defaultuser=201  
secret=pass  
密碼  
canreinvite=no  
host=dynamic  



[Asterisk基本設定ガイド]:http://www.st-asterisk.com/