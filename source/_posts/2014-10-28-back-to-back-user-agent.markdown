---
layout: post
title: "何謂 Back-to-back user agent ?"
date: 2014-10-28 23:49:06 +0800
comments: true
categories: ["sip"]
---

<!-- more -->

在 RFC3261 裡面有定義何謂 Back-to-back user agent （B2BUA）? 是讓 client 端可以透過 B2BUA 使用 sip 協定建立連線，
然後必須要一直保持連線， 以角色來說就像  FreeSWITCH 一樣，就算是使用 sip 建立連線之後利用 rtp 傳送訊息似乎也需要
 FreeSWITCH 幫忙，我原本以為 FreeSWITCH 只是幫忙建立連線但從規格書上看還是需要 FreeSWTICH 參與對話。



