---
layout: post
title: "vSphere Centos 更改網卡"
date: 2014-08-18 22:51:39 +0800
comments: true
categories: ["linux"]
---

<!-- more -->


使用 vSphere 的樣板 deploy 一個新的虛擬機器的時候會自動建分配一個 IP 給網卡，但是網卡卻是 eth1也無法直接指定固定 ip 所以需要修改下面這支檔案。


	[root@localhost ~]# vim /etc/udev/rules.d/70-persistent-net.rules

裡面有對應的網卡名稱和 MAC 位址，將對應的網卡名稱改到 eth0 並且將 eth0 MAC 位址修改下面的檔案
裡面，並且設定成 static 和指定 IP 然後重開機可以看到效果了。

	[root@localhost ~]# vim /etc/sysconfig/network-scripts/ifcfg-eth0