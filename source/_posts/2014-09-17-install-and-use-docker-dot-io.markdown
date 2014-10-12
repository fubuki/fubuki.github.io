---
layout: post
title: "install and use docker.io"
date: 2014-09-17 23:35:45 +0800
comments: true
categories: ["docker"]
---

在 Centos 下安裝和使用 docker.io。

<!-- more -->


### 安裝
	Centos
	yum install docker-io
	service docker start

	Ubuntu
	curl -sSL https://get.docker.io/ubuntu/ | sudo sh
### 使用
	docker pull centos
	docker run centos:latest cat /etc/centos-release


### 建立 LAMP 環境

docker-io 藉由映像檔建立環境，所有想說可不可以藉由 docker 快速建立 LAMP 的環境，在網路上找了一下有人寫了類似的東西，
[これから始める「DockerでかんたんLAMP環境 for CentOS」] 和 [docker-centos-lamp] 作為參考。

[これから始める「DockerでかんたんLAMP環境 for CentOS」]:http://knowledge.sakura.ad.jp/tech/1811/
[docker-centos-lamp]:https://github.com/kunihirotanaka/docker-centos-lamp