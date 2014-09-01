---
layout: post
title: "rebar 備忘錄"
date: 2014-08-26 23:32:46 +0800
comments: true
categories: ["erlang"]
---

<!-- more -->

###安裝

	git clone https://github.com/rebar/rebar
	cd rebar
	./bootstrap
	sudo mv rebar /usr/local/bin 


###建立一個 app
	
	rebar create-app appid=erl-app

###編譯

	rebar compile

[rebar]:https://github.com/rebar/rebar