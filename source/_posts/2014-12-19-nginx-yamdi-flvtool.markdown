---
layout: post
title: "添加 Flv  keyframes 支持拖動撥放"
date: 2014-12-19 22:36:50 +0800
comments: true
categories: ["linux"]
---


<!-- more -->

目前在研究在多種裝置上面支援播放影片，目前看到有使用下面幾種方式:

1. RTMP/RTMPT
2. RTSP
3. HTTP
4. MMS
5. HLS

而手上有 mp4 和 flv 以及 m3u8 三種格式需要播放，目前是先選用 nginx 透過 HTTP 播放這樣需要安裝的套件比較少，
如果要使用 CDN 擴展也比較方便，但是除了原本的 m3u8 格式可以支援拖動撥放，另外兩個要使用其他工具添加 keyframes 才能讓
播放器不需要載入全部檔案就可以撥放，下面記錄目前有使用哪些工具添加 keyframes。


### flv
1. [yamdi]
2. [flvtool++]

### mp4
1. [qtfaststart]
2. MP4Box

[yamdi]:http://yamdi.sourceforge.net/
[flvtool++]:https://github.com/Elbandi/flvtool-pp
[qtfaststart]:https://github.com/danielgtaylor/qtfaststart
[libstreaming]:https://github.com/fyhertz/libstreaming
