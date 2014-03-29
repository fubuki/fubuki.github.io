---
layout: post
title: "node-gyp build fails on NFS because of flock"
date: 2014-03-23 00:00:00 +0800
comments: true
categories: ['nodejs']
---

在下載一些使用node-gyp編譯的模組會遇到問題，後來發現在一些檔案系統會出問題，可以在這邊[issue]找到解答。


[issue]: https://github.com/TooTallNate/node-gyp/issues/147
