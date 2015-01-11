---
layout: post
title: "Lighttpd 搭配 Fastcgi 和 Webpy"
date: 2014-12-12 00:18:20 +0800
comments: true
categories: ["python"]
---


<!-- more -->

最近在研究別人寫的專案看到使用 Lighttpd 跑 Python 的程式碼，透過 Fastcgi 跟 Python 程式碼溝通， 
Python 端則是使用 [Webpy]，環境可以參考 [Webpy + LightTTPD with FastCGi]。


	apt-get install lighttpd
	vim /etc/lighttpd/lighttpd.conf

 	fastcgi.server = ( "/app.py" =>
 	(( "socket" => "/tmp/fastcgi.socket",
    	"bin-path" => "/var/www/html/app.py",
    	"max-procs" => 1,
   		"bin-environment" => (
     	"REAL_SCRIPT_NAME" => ""
   		),
   		"check-local" => "disable"
 	))
 	)

 	easy_install web.py

[Webpy]:http://webpy.org
[Webpy + LightTTPD with FastCGi]:http://webpy.org/cookbook/fastcgi-lighttpd