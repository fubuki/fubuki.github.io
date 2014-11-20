---
layout: post
title: "Facebok Messenger 的 新架構"
date: 2014-10-25 22:44:32 +0800
comments: true
categories: ["mqtt"]
---


<!-- more -->

Facebook 更改他們的 Messageer 的背後架構，在 [Building Mobile-First Infrastructure for Messenger] 一文中有提到做了哪些更改並且提到更改後提升的多少效能。

裡面其中一個引我注意的是使用 mqtt + thrift 和 iris，工作上原本有使用 mqtt 當作 server 與 client 之間溝通的協定，但是在傳輸量上面希望能夠在縮減一些，目前看到有人提到 mqtt + protobuf 和 mqtt + thrift，主要都是使用 mqtt 載體然後利用其他方式壓縮訊息內容，Facebook 似乎是用 thrift 壓縮訊息內容，也許可以嘗試看看。


另外一個是 Facebook 採用 'push-based snapshot + delta model'，這個 model 是使用 iris 實現，似乎是一種 message queue，裡面有兩個指針指向 APP 最後收到的訊息和 server 最新收到的訊息，之前有計畫寫個類似的東西用來存放使用者訊息，也許可以參考一下 Facebook 的架構。



[Building Mobile-First Infrastructure for Messenger]:https://code.facebook.com/posts/820258981365363/building-mobile-first-infrastructure-for-messenger/