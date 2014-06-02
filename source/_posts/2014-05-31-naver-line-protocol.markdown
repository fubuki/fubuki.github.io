---
layout: post
title: "NAVER  Line Protocol"
date: 2014-05-31 22:38:23 +0800
comments: true
categories: ["LINE"]
---

研究關於Line 的通訊架構。

<!-- more -->

目前可以知道Line 有使用 SPDY ，不過[emulating-the-line-application]有提到也有使用thrift用來控制訊息的部分，
另外透過[purple-line]這個專案也能稍微了解Line的應用程式與伺服器之間互相通訊的過程，裡面也有一份[line-protocol]的
規格表可以做為日後開發類似功能的參考。

[emulating-the-line-application]:http://blogs.ixiacom.com/ixia-blog/emulating-the-line-application/
[purple-line]: https://github.com/mvirkkunen/purple-line
[line-protocol]: http://altrepo.eu/git/line-protocol.git/