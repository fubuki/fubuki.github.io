---
layout: post
title: "讓 crontab 執行 30 秒任務"
date: 2014-12-07 10:48:17 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

crontab 是 linux 用來執行定時任務的指令，但是他最多只能指定到分，如果要有設定 30 秒執行的任務就要比較特殊的做法。


使用 sleep 指令延遲 30 秒執行，這樣就可以達成每 30 秒執行任務的功能。

	* * * * * ntpdate -s time.stdtime.gov.tw
	* * * * * sleep 30 &&  ntpdate -s time.stdtime.gov.tw
