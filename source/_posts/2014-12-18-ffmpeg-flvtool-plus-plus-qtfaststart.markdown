---
layout: post
title: "在 Centos 6 安裝 ffmpeg flvtool++  qtfaststart"
date: 2014-12-18 22:43:14 +0800
comments: true
categories: ["linux"]
---


<!-- more -->

#### ffmpeg

在 Centos 上面使用 yum 安裝的 ffmpeg 版本都太舊了，版本只有到 0.6 而已目前最新已經到 2.5 了，
另外使用 yum 安裝的 ffmpeg 似乎沒有把一些我需要的編碼加進去導致沒有支援 flv 的轉碼。

目前看到網路上有很多教程解說如何從原始碼安裝 ffmpeg ，但是在編譯的時候在跑 x264 的時候就沒有辦法通過編譯
，最後參考這篇 [Install FFMpeg] 才能編譯過去。看起來也許是之前的函式庫沒有移除乾淨所導致的。

下面兩個是讓 mp4 和 flv 檔案可以透過 http 的方式拖動撥放


#### qtfaststart 

[qtfaststart] 是用來轉 mp4 的相關工具，直接透過 pypi 安裝即可。

	easy_install qtfaststart


#### flvtool++

網路上有 [flvtool++] 和 flvtool2 這兩者似乎是類似的東西用來處理 flv 檔案， yum 源裡面是有 flvtool2
[flvtool++] 只能自行編譯安裝。


[Install FFMpeg]:http://wiki.razuna.com/display/ecp/FFMpeg+Installation+on+CentOS+and+RedHat
[qtfaststart]:https://github.com/danielgtaylor/qtfaststart
[flvtool++]:https://github.com/Elbandi/flvtool-pp