---
layout: post
title: "LINE 的 安全性問題"
date: 2014-09-25 22:32:14 +0800
comments: true
categories: ["LINE"]
---

關於 LINE 的安全性問題。

<!-- more -->

日前看到在日本媒體有在報導韓國的國家情報局透過 LINE 收集訊息的事情，最後是由 LINE 的社長出面澄清此事，不過這讓我想去
了解一下 LINE 在通信上是如何加密的保障他的安全性。

LINE 是使用 SPDY + thrift 傳輸資料，而 SPDY 是基於 TLS 實現的本身就有加密，不過在舊的版本似乎沒有全部都走 TLS，在 LINE 的
開發 BLOG 上有寫說由於 TLS 在移動網路上會增加連接時間和導致傳輸異常便允許沒加密的網路連線，不過後面有寫在 3.9.3 版本之後全部都走
加密連線，似乎是透過 RSA 2048 bit 加密。

	Updated on 2014/06/21: LINE 3.9.3 or newer versions encrypt all message data even on mobile network like 2G, 3G and LTE

另外在 BLOG 的文章裡也有提到其他關於安全性的事情，不過在 Server 的資料加密就沒有提到太多的部分。



###參考文章
1. [LINE「独自暗号化」のメリットと安全性について]
2. [LINE Security – Simple, Safe, Secure]
3. [LINEの暗号化について]
4. [Android版LINE Appの通信を覗いてみる]

[LINE「独自暗号化」のメリットと安全性について]:http://blog.kazuhooku.com/2014/06/line.html
[LINE Security – Simple, Safe, Secure]:http://developers.linecorp.com/blog/?p=2709
[LINEの暗号化について]:http://developers.linecorp.com/blog/?p=3262
[Android版LINE Appの通信を覗いてみる]:http://inaz2.hatenablog.com/entry/2014/07/03/000900
