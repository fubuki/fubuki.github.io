---
layout: post
title: "安裝 Coreos"
date: 2014-12-01 01:19:28 +0800
comments: true
categories: ["docker"]
---


<!-- more -->

Coreos 在官網提供了不少安裝方式，我是使用它提供的 VMware 的映像檔安裝，下載之後解壓縮使用 VMware 啟動。

	curl -LO http://alpha.release.core-os.net/amd64-usr/current/coreos_production_vmware_insecure.zip

下載的檔案裡面有個 `insecure_ssh_key`，這個映像檔裡面沒有提供帳密登入預設你要用公私鑰登入，我這邊使用
`puttygen.exe` 載入 `insecure_ssh_key` 生成 putty 所吃的格式後使用 `core` 當作登入帳號便可以登入。

	docker run -t -i ubuntu /bin/bash


整個映像檔大小不到 200M  架設起來很方便，目前有看到有公司考慮要將系統移除 docker 裡面利用 Coreos 建立環境，
這也許可以參考未來架構的規劃。



