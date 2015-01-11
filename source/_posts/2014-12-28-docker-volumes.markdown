---
layout: post
title: "Docker 的 Volumes 功能"
date: 2014-12-28 22:51:26 +0800
comments: true
categories: ["docker"]
---

<!-- more -->

最近在用 Docker 建立的 FFmpeg 的容器時，想要建立的直接在容器裡面寫入檔案執行轉檔，然後看到了 Docker 有類似掛載的功能，
可以建立 Volumes 讓各個不同的容器共用，之後如果有升級或是跟其他容器結合形成一個服務平台可以採取這樣的做法。


另外有看到一篇蠻有趣的文章 : [How to deal with persistent storage (e.g. databases) in docker]，裡面的回答有提到一個東西
 `data only container`，似乎是建立一個專門掛載 Volumes 的 container ，從這篇 [Tiny Docker Pieces, Loosely Joined] 最後面
 有提到一些關於這樣做法的好處，似乎是能更好管理 Volumes 裡面的內容。




[How to deal with persistent storage (e.g. databases) in docker]:http://stackoverflow.com/questions/18496940/how-to-deal-with-persistent-storage-e-g-databases-in-docker
[Tiny Docker Pieces, Loosely Joined]:http://www.offermann.us/2013/12/tiny-docker-pieces-loosely-joined.html