---
layout: post
title: "nodejs flow control"
date: 2014-04-06 16:22:06 +0800
comments: true
categories: ['nodejs']
---
記錄一下流程控制相關的模組。  
1. [step]   
2. [Q]  
3. [promise]  
<!-- more -->

由於nodejs是非同步的，所以流程控制是很重要的一部分，一般撰寫程式時會等待其他區塊的回傳參數，但是由於非同步的關係所以需要以嵌套的方式
避免所需要的參數尚未回傳就執行下一步的函式導致未知的結果，如此一來就會出現多重嵌套的情形導致程式以後變的難以除錯並且看起來也很醜，所以
有些人提供一些第三方的模組處理流程控制的部分。



[step]: https://github.com/creationix/step
[Q]: https://github.com/kriskowal/q
[promise]: https://github.com/kriszyp/node-promise 