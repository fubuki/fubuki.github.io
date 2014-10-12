---
layout: post
title: "asterisk realtime architecture"
date: 2014-10-07 23:32:11 +0800
comments: true
categories: ["sip"]
---

<!-- more -->

asterisk 可以透過 ODBC 跟 MySQL 連線然後在 MySQL 動態修改 sip user 的資訊，藉此不需要在 conf 裡面設定 sip user 的資訊。
