---
layout: post
title: " php-fpm 優化參數"
date: 2014-07-01 23:30:29 +0800
comments: true
categories: ["php"]
---

warning pool www child exited on signal 9 (sigkill) after seconds from start

<!-- more -->

php-fpm管理進程的模式有靜態和動態，差別在於靜態會根據參數直接生成固定的進程，動態則是會動態調整所需要的進程，
選擇哪個模式端看於硬體上記憶體大小的差別。



##靜態或是動態
pm = static or dynamic  

##靜態方法
pm.max_children : php-fpm 最大進程數  


##動態方法
pm.start_servers : php-fpm 一開始創鍵的進程數  

pm.min_spare_servers : php-fpm 最小的進程數

pm.max_spare_servers : php-fpm 最大進程數


##其他參數

pm.max_requests : 一個進程處理多少個請求後就重新啟動


##參數大小設定規則