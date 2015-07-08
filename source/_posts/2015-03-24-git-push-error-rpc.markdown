---
layout: post
title: "git push 出現 rpc error"
date: 2015-03-24 21:33:53 +0800
comments: true
categories: ["git"]
---


<!-- more -->

最近在推專案上 Github 的時候出現 rpc error 的問題，後來找網路上的解法是說
 Buffer 開太小了所以需要增加，增加的方法是用下面的指令。


	git config http.postBuffer xxxxxxxxx