---
layout: post
title: "Android NDK 環境建立"
date: 2014-09-02 23:53:40 +0800
comments: true
categories: ["android"]
---

<!-- more -->


如何建立 Android 使用 NDK 的環境。

1. ADT
2. NDK
3. cygwin


下載 Eclipse + ADT 就建立好基本的開發環境，在來下載 NDK 後在 Eclipse 指定 NDK 路徑，原本NDK 在 windows 環境下需要 cygwin 才能編譯。
但是在 R7 之後的版本就內帶編譯環境而不需要 cygwin 的樣子，而舊版的 NDK 可以安裝 [mini-cygwin] 建立編譯環境取代安裝龐大的 cygwin。



[mini-cygwin]:https://code.google.com/p/mini-cygwin/