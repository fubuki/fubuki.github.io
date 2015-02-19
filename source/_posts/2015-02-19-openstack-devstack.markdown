---
layout: post
title: "透過 Devstack 使用 Openstack "
date: 2015-02-19 19:27:47 +0800
comments: true
categories: ["openstack"]
---


<!-- more -->

如果想要測試看看 Openstack 的功能，可以先使用 [Devstack] 在一台機器上面建立環境，可以免去很多麻煩的設定。

我是在 ubuntu 14.04 的虛擬機器裡面執行，安裝方式主要是取得 [Devstack] 後使用非 root 帳號執行 `stack.sh` 腳本，
另外這邊需要在 `/etc/sudoers` 設定本帳號在使用 sudo 時無需輸入密碼，然後在重新開機後需要使用 `rejoin-stack.sh` 啟動服務。  



#### Install
	git clone https://github.com/openstack-dev/devstack.git
	cd devstack
	./stack.sh

#### Minimal Configuration

	[[local|localrc]]
	ADMIN_PASSWORD=secrete
	DATABASE_PASSWORD=$ADMIN_PASSWORD
	RABBIT_PASSWORD=$ADMIN_PASSWORD
	SERVICE_PASSWORD=$ADMIN_PASSWORD
	SERVICE_TOKEN=a682f596-76f3-11e3-b3b2-e716f9080d50

[Devstack]:https://github.com/openstack-dev/devstack