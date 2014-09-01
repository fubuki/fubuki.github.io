---
layout: post
title: "使用 cnpm 建立私有的 npm 服務"
date: 2014-08-30 23:40:10 +0800
comments: true
categories: ["nodejs"]
---

<!-- more -->


[cnpm] 可以讓使用者建立給企業用的 npm 服務，由於公司政策的關係有時候連接 npm 服務會有問題，
並且如果有自製的套件有發布到多台機器上會有點麻煩，藉此可以利用 [cnpm] 加速下載並且避開一些
機器連網的問題。

[cnpm]:http://cnpmjs.org/