---
layout: post
title: "CQRS Architecture"
date: 2015-06-23 00:52:40 +0800
comments: true
categories: ["architecture"]
---

<!-- more -->

最近在研究一些秒殺活動的架構，看到有人提到 [CQRS] 這種模式，之前看過國外在金融系統上使用 LMAX 的架構
其實就是一種 [CQRS] 模式也就是讀寫分離，讀取和寫入分成兩種架構，然後使用像是 LMAX 裡面提到的 EVENT SOURCE 的模式，
類似 git 裡面的 commit 的概念，將所有的修改視為一種事件存放起來。

這樣的模式通常我會使用 message queue 存放寫入的事件然後利用多個 worker 處理這些寫入事件將資料直接寫入資料庫，所以在某些情形
下負責讀取資料的部分可能會因為延遲寫入導致會查詢不到一些資料。

有些記錄可能會大量更新，哪些部分就放在記憶體中處理，如果有遇到當機之類的災難可能要從 message queue 的部分將資料重新寫回記憶體，
所以有可能需要就 message queue 的事件另外存放一段時間直到資料都寫回到資料庫裡。


[CQRS]:http://martinfowler.com/bliki/CQRS.html