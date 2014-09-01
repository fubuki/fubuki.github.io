---
layout: post
title: "rabbitmq http api"
date: 2014-08-13 23:51:29 +0800
comments: true
categories: ["rabbitmq"]
---


<!-- more -->

rabbitmq 的 Management Plugin 提供了 http 的接口讓開發者可以透過 API 控制， 直接透過 Management Plugin 提供
的後台速度不太能恭維， 並且希望能夠透過這些 API 管理 rabbitmq裡的 queue。
