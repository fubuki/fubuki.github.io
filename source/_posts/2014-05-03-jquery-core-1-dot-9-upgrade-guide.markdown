---
layout: post
title: "jQuery Core 1.9 Upgrade Guide"
date: 2014-05-03 19:07:00 +0800
comments: true
categories: ["javascript"]
---
jQuery升級到1.9需要注意的事項。
<!-- more -->

詳細的內容在官網的[1.9 Upgrade Guide]有詳細說明，目前網站最常用的通常是1.7的版本，
如果要遷移到1.9的版本要注意一下，因為1.9版本改變幅度蠻大的，之前在工作中一些寫法和
plugin就沒有辦法使用就降級到1.8版本，不過也能夠使用[jquery-migrate]讓開發者使用
以前的特性，但是要注意有些特性就算裝上plugin也無法復原。

## 記錄一下工作上影響比較大的部分

1. 拿掉.toggle(function, function, ... ) 的用法，
2. 拿掉 jQuery.browser() 使用 Modernizr偵測閱覽器是否支援這個功能比較好。
3. 拿掉 live換用 on 。
4. 拿掉 die 換用 off 。
5. Ajax 的全域事件要綁在document上面。
6. jQuery(htmlString) versus jQuery(selectorString)
7. .attr() versus .prop()
8. $("input").attr("type", newValue) in oldIE
9. "hover" pseudo-event
10. 移除一些jQuery沒有寫出來了函式拿掉 例如:jQuery.clean()。 


[1.9 Upgrade Guide]: http://jquery.com/upgrade-guide/1.9/
[jquery-migrate]: https://github.com/jquery/jquery-migrate