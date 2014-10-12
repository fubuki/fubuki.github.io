---
layout: post
title: "Sip Library"
date: 2014-10-06 23:24:07 +0800
comments: true
categories: ["sip"]
---

<!-- more -->

最近想在手機上實現音訊通話的功能，之前有想過使用 ejabberd + xmpp 實現，不過後來還是使用 SIP 實現，剩下來的問題便是要
怎麼在手機上實現 SIP 的協定，目前在考慮的有下面三個選擇，不過其中 [liblinphone] 非常大，我傾向於使用 [pjsip] 和 [doubango]，
另外在看 SIP 的時候意外發現也跟 webrtc 有關， web 方面如果有支援 webrtc 便能讓閱覽器透過 sip server 跟手機聊天。


1. [pjsip]
2. [liblinphone]
3. [doubango]




[pjsip]:http://www.pjsip.org/
[liblinphone]:http://www.linphone.org/technical-corner/liblinphone/overview
[doubango]:http://doubango.org/
