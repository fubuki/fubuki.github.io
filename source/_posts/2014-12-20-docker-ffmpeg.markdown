---
layout: post
title: "使用 Docker 建立 FFmpeg 環境"
date: 2014-12-20 22:33:21 +0800
comments: true
categories: ["docker"]
---

<!-- more -->

 之前在安裝 FFmpeg 的時候吃了不少苦頭，然後未來也有可能會需要更新一些已經有安裝的 Server，所以嘗試一下使用 docker 建立
  ffmpeg 環境，目前有找到 [cellofellow/ffmpeg] 這個 docker file 可以使用， docker file 安裝指令如下:

  	docker pull cellofellow/ffmpeg  
  	docker run -i -t cellofellow/ffmpeg /bin/bash

安裝後進去就可以使用最新版的 ffmpeg 下面是他的編譯參數目前手上會用的編碼都有包進去了，比較有問題的是 `libfdk-aac` 與
 `libfaac` 的差別，兩個似乎都是用來解 FAAC 的，不過從網路上的資訊來看是 libfdk-aac 比較好。

	configuration: 
	--extra-libs=-ldl 
	--enable-gpl 
	--enable-libass 
	--enable-libfdk-aac 
	--enable-libmp3lame 
	--enable-libopus 
	--enable-libtheora 
	--enable-libvorbis 
	--enable-libvpx 
	--enable-libx264 
	--enable-libx265 
	--enable-nonfree

題外話在網路上有看到 Cookpad 也有用 docker 建立影音轉碼平台 : [Dockerでffmpegもimagemagickも怖くないという話]，
裡面的的 docker file 也有放出來 [janiConverter] 讓人使用。



[janiConverter]:https://github.com/cookpad/janiConverter
[cellofellow/ffmpeg]:https://registry.hub.docker.com/u/cellofellow/ffmpeg/
[Compile FFmpeg on Ubuntu, Debian, or Mint]:https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu
[Dockerでffmpegもimagemagickも怖くないという話]:http://techlife.cookpad.com/entry/ffmpeg_and_imagemagick_setup_with_docker