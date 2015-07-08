---
layout: post
title: "安裝和使用 Ceph"
date: 2015-06-10 22:10:38 +0800
comments: true
categories: ["openstack"]
---

<!-- more -->


### 環境

ubuntu 14.04 LTS

### 安裝

	把 ceph 的 package 加入
	wget -q -O- https://raw.github.com/ceph/ceph/master/keys/release.asc | sudo apt-key add -
	echo deb http://ceph.com/debian/ $(lsb_release -sc) main | sudo tee /etc/apt/sources.list.d/ceph.list

	更新 index 和安裝 ceph
	sudo apt-get update && sudo apt-get install ceph

#### 建立設定檔

	vim /etc/ceph/ceph.conf

	[osd]
		osd journal size = 1000
		filestore xattr use omap = true

	[mon.a]

		host = {hostname}
		mon addr = {ip-address}:6789

	[osd.0]
		host = {hostname}

	[osd.1]
		host = {hostname}

	[mds.a]
		host = {hostname}

#### 建立資料夾

	sudo mkdir /var/lib/ceph/osd/ceph-0
	sudo mkdir /var/lib/ceph/osd/ceph-1
	sudo mkdir /var/lib/ceph/mon/ceph-a
	sudo mkdir /var/lib/ceph/mds/ceph-a

	cd /etc/ceph
	sudo mkcephfs -a -c /etc/ceph/ceph.conf -k ceph.keyring


### 使用
根據官網的安裝方式很簡單，但是要啟動的時候遇到一些問題，下面列了幾個遇到的問題。

	Error ENOENT: osd.0 does not exist.  create it before updating the crush map
	ceph osd create

	ceph health
	HEALTH_WARN 384 pgs incomplete; 384 pgs stuck inactive; 384 pgs stuck unclean
	ceph pg dump_stuck stale && ceph pg dump_stuck inactive && ceph pg dump_stuck unclean

	HEALTH_WARN 384 pgs incomplete; 384 pgs stale; 384 pgs stuck inactive; 384 pgs stuck unclean; 35 requests are blocked > 32 sec

	HEALTH_WARN 384 pgs incomplete; 384 pgs stuck inactive; 384 pgs stuck unclean; 35 requests are blocked > 32 sec; mon.a low disk space