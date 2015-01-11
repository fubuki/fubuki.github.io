---
layout: post
title: "Canvas Fingerprinting"
date: 2014-12-05 21:56:17 +0800
comments: true
categories: ["frontend"]
---

<!-- more -->

以前的網站都是使用 cookie 追蹤使用者所以現在的閱覽器通常會提供私密模式讓網站無法在機器
上寫入 cookie，所以最近看到有網站使用 [Canvas fingerprinting] 的技術追蹤用戶。


[Canvas fingerprinting] 的原理是用 html5 的 Canvas 功能繪製圖片產生識別碼，由於每台機器
在繪製圖片的時候所使用繪製引擎和參數不同所以使用產生出的圖片便不會全部相同，在經過 hash 
之類的操作得出的編碼就可以用來當作識別用戶的一種方法。


這邊有一篇相關論文可以參考 [Pixel Perfect: Fingerprinting Canvas in HTML5]。

[Canvas fingerprinting]:http://en.wikipedia.org/wiki/Canvas_fingerprinting
[Pixel Perfect: Fingerprinting Canvas in HTML5]:http://cseweb.ucsd.edu/~hovav/papers/ms12.html