---
layout: post
title: "mosquitto bridge conf"
date: 2014-06-10 22:04:53 +0800
comments: true
categories: ["mqtt"]
---

記錄一下 mosquitto bridge config的部分
<!-- more -->


cleansession

當網路斷線的時候要不要清掉remote broker的連線資訊和訊息，預設是 false，但是不論是true 或是 false在某些情形下都會有問題。


round_robin 
如果有多個bridge server 當第一個server當掉就會跳第二個server，然後會有兩種情形，會不會一直去測試第一個server能不能
連接，或是直到當第二個server當掉才會去連接第一個server。


start_type [ automatic | lazy | once ]

automatic 會自動連接上bridge server。

lazy 當收到的訊息超過一個門檻才會連接bridge server 當經過一個idle timeout 會斷開連結，這是為了在
使用者只希望有需要發送訊息的時候才會連接 server

once 會自動連接bridge server但是如果連接失敗就不會重連接。


threshold count
給start_type lazy使用，當收到多少訊息才會重開(從上面來看應該是連接bridge server才對)


topic pattern [[[ out | in | both ] qos-level] local-prefix remote-prefix]


topic # both 2 local/topic/ remote/topic/


有哪些 topic會被分享給其他broker，並且可以重新對應topic的部分。


try_private [ true | false ]

設定這個server是一個bridge或是一個普通的客戶端，如果是這個sever是一個bridge會有loop detection，
因此會消耗一些效能。









