---
layout: post
title: "memcached repcached"
date: 2014-10-30 21:43:51 +0800
comments: true
categories: ["memcached"]
---


<!-- more -->

最近在看 memecached 架構的時候發現了一個名叫 [repcached] 的東西，似乎日本那邊基於 memecached 開發出來的擴充版本，
每台 memcached 都是 master 並且能夠互相同步，這邊有關於 repcached 的[說明]，跟之前使用 twemproxy 和 lib-memcached 擴展的方式不一樣，
可以研究一下其中的機制。




[repcached]:http://repcached.lab.klab.org/
[說明]:https://www.nic.ad.jp/ja/materials/iw/2008/proceedings/F2/IW2008-F2-08.pdf