---
layout: post
title: "rabbitmq auth plugin"
date: 2014-11-05 22:49:35 +0800
comments: true
categories: ["rabbitmq"]
---

<!-- more -->


在使用 rabbitmq 建立系統時，由於會將 rabbitmq 暴露在外層所以需要認證 client 是否合法，原本 rabbitmq 提供的認證方式並不適合讓
 client 都有自己的帳密進行認證，所以有想過撰寫一個中間層在 client 和 rabbitmq 之間進行認證，不過後來找到了 [rabbitmq-auth-backend-http]
 原來可以透過 rabbitmq plugin 擴增認證的方式，更仔細查詢似乎是跟 `SASL Authentication` 看來是 rabbitmq 已經有提供類似的機制給開發者了只是我沒有
 注意到而已。





[RabbitMQ - Plugin Development Guide]:https://www.rabbitmq.com/plugin-development.html
[rabbitmq-auth-backend-http]:https://github.com/simonmacmullen/rabbitmq-auth-backend-http