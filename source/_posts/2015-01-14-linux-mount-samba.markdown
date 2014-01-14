---
layout: post
title: "linux 掛載 Samba 目錄的方法"
date: 2015-01-14 23:19:07 +0800
comments: true
categories: ["linux"]
---


<!-- more -->

最近幫人建立一個根據正式機的鏡像系統，需要掛載在多台主機掛載相同的目錄，所以紀錄一下掛載的方法，
以前有用 `smbfs` 掛載但是比較新的版本似乎只能用 `cifs`。


	mount -t cifs -o username="root",password="toor" //host ip/srv /srv
	umount /srv