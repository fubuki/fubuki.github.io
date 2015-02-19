---
layout: post
title: "Node apns ECONNRESET"
date: 2015-02-05 23:43:26 +0800
comments: true
categories: ["nodejs"]
---


<!-- more -->

最近在使用 node-apn 建立推播 Server 的時候遇到了一個問題，如果一段時間沒有發送推播會出現 `ECONNRESET` 的錯誤訊息，
在使用 node-gcm 的時候不會出現這樣的錯誤訊息，然後在 github 有人也有遇到相同的 [issue]，目前似乎需要設置一個 timeout 主動
斷線後，自行重新連線。



[Node js ECONNRESET]:http://stackoverflow.com/questions/17245881/node-js-econnreset
[issue]:https://github.com/argon/node-apn/issues/137