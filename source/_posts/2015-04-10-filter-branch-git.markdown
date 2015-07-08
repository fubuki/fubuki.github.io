---
layout: post
title: "git filter-branch"
date: 2015-04-10 23:06:20 +0800
comments: true
categories: ["git"]
---


<!-- more -->


`git filter-branch‵ 能夠改寫整個專案的歷史，會用到這個是因為以前有人在專案裡面將很多
二進位檔案加入追蹤導致專案過於肥大，另外裡面有些檔案帶有敏感資訊所以必須連 commit 裡面的
訊息全部去除，這時就用到 `git filter-branch‵ 。
