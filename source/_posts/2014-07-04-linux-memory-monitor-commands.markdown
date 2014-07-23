---
layout: post
title: "linux memory monitor commands"
date: 2014-07-04 23:20:56 +0800
comments: true
categories: ["linux"]
---

記錄監控linux主機記憶體使用量的命令。

<!-- more -->


1. `free -m`
2. `ps aux --sort -rss`
3. `ps -ylC xxx --sort:rss | awk '{sum+=$8; ++n} END {print "Tot="sum"("n")";print "Avg="sum"/"n"="sum/n/1024"MB"}'`
4. `netstat -an | awk '/^tcp/ {++s[$NF]} END {for(a in s) print a, s[a]}'`
5. `top`