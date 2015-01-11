---
layout: post
title: "Aeron message protocol"
date: 2014-12-16 23:24:50 +0800
comments: true
categories: ["architecture"]
---

<!-- more -->


最近發現了一個跟消息系統有關的的開源專案: [Aeron] ，目前已經手上是用過好幾種消息系統每種都有他們的特性，
所以是否還需要另外新的消息系統? 這篇 [Aeron: Do we really need another messaging system?] 可以讀讀，了解
跟為何開發這個系統。


上面的文章有提到其他消息系統像是瑞士刀， [Aeron] 則像是一把手術刀，沒有提供太多功能，並且是放在 tcp 的層級使用，
看起來是用來建立系統低階的部分高階的部分在讓開發者另外去解決，這讓我感覺有點像 zeroMQ 但是文章裡面卻說是不一樣的東西。


[Aeron]:https://github.com/real-logic/Aeron
[Aeron: Do we really need another messaging system?]:http://highscalability.com/blog/2014/11/17/aeron-do-we-really-need-another-messaging-system.html