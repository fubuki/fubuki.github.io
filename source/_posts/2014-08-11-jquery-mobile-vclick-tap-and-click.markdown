---
layout: post
title: "jQuery mobile vclick , tap and click"
date: 2014-08-11 22:52:44 +0800
comments: true
categories: ["javascript"]
---

<!-- more -->

工作上有需要製作Mobile Device用的網頁，以前有聽過有些閱覽器有些事件是不太一樣的，特此在這
紀錄一下幾種點擊事件。
可以參考[in-jquery-mobile-whats-the-diff-between-tap-and-vclick]


###Click
手機和桌面閱覽器都有支援，在 `android` 會有 Visible delay

###Tap
只有手機閱覽器支援, no delay

###VClick
手機和桌面閱覽器都有支援 no delay

目前看到有人同時使用 `click` 和 `vclick` 綁定，使用上要注意的應該是 Visible delay。

[in-jquery-mobile-whats-the-diff-between-tap-and-vclick]:http://stackoverflow.com/questions/15274809/in-jquery-mobile-whats-the-diff-between-tap-and-vclick