---
layout: post
title: "node.js 0.12 版本"
date: 2014-04-16 23:18:11 +0800
comments: true
categories: ["nodejs"]
---

nodejs 0.12版本出來了，多了一些新的API，改進Cluster的功能此外ES6 的特性在0.11.9也可以開啟使用。
<!-- more -->

###Cork support for writable streams
這邊是提升tcp傳輸的效率，當數據流裡面的小數據結合成大數據在送出減少tcp和系統的調用。

###tls module
原本nodejs的tls模塊的效率提高了，之前有使用過http模組的tls功能不過沒有測試過他的效率。

###Crypto performance improvements
改進加解密演算法的速度，不過我比較常用的主要在session方面的加密
###Reduced garbage collector strain
0.12版本改寫了關於context的部分[multi-context refactoring]，藉此減少v8在multi-context的情形下，
不會讓V8一直處理關於handle的問題。

###Better cluster performance
這個改進我有可能比較常用到，目前在作nodejs applicacion的架構優化並且希望機器的資源能充分使用，然後這篇[post]有提到
如何改進cluster的效率。

### Faster timers, faster setImmediate(), faster process.nextTick()
這部分是提升像是setTimeout之類API的效率，這裡就不太清楚了。


原文在此[node-js-v-0-12-whats-new]

[node-js-v-0-12-whats-new]: http://strongloop.com/strongblog/performance-node-js-v-0-12-whats-new/
[multi-context refactoring]: https://github.com/joyent/node/commit/756b622
[post]: http://strongloop.com/strongblog/whats-new-in-node-js-v0-12-cluster-round-robin-load-balancing/