---
layout: post
title: "nodejs 生產環境"
date: 2014-04-05 21:55:23 +0800
comments: true
categories: ['nodejs']
---

記錄一下nodejs生產環境需要注意的事項。
<!-- more -->

1. nodejs是非同步但是也有一些同步的API(例如讀取檔案)會影響nodejs的運行，要小心使用那些API。
2. nodejs底層是使用V8引擎可以藉由調整V8的GC策略提升效能。
3. nodejs建立socket時增加可以建立的socket的數量。
4. nodejs 有些使用模組是編譯過的，有些是純js撰寫成的，使用二進位編譯後的模組。
5. 在nodejs中事件流的處理會影響程式效能，目前有些用來處理事件流的模組慎選並去使用。
6. nodejs的session通常使用express處理，預設存放在記憶體內，建議替換到redis或是memcache的資料庫存放。