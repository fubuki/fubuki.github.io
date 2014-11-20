---
layout: post
title: "PHPConf Taiwan 2014"
date: 2014-10-18 21:44:03 +0800
comments: true
categories: ["open source"]
---

<!-- more -->

### 新浪微博 LAMP 優化之路
PHP NG 主要作者  
每天20憶pv 50億 hits  
400台前端機器  

####2012年3月
使用 apache + php

17w 行代碼導致很難維護

1. 性能優化
2. 架構優化
3. 基礎優化
4. 遠程優化

Yaf c base framework 類似 phalcon
只實現基本功能
不需要 ORM

####Weibo 擴展
1. Weibo conf 
2. Weibo Utils 

棄用 Smarty

####結構優化 -解耦
1. Pagelate
2. Bigpipe

soa 的形式

####結構優化 - Yar rpc framewrok

第一個 php和 rpc 並行的框架

CBigpipe 加速

前端 PHP 後端 C

升級 PHP 5.4

LAMP => LNMP

踩了一些坑

使用 Zend Optimizer Plus (O+) 替換 apcache

快於7% 到 10%
####性能優化 Yac

主要是無鎖共享
使用 CRC 校驗資料使否出錯的問題

####移動微博

移動佔到 70%以上

服務器 cpu idel 5%

PHP 異步調用

jsond 

L0 和 L1 兩種類型的快取，分成本機和全域兩種

為何使用無鎖? key 包含 CRC ，使用CRC跟值校驗 降低錯誤率

### 專案管理

本職 PM  
學生症候群  
寫書經驗  

####領導力 
冒險心
跳脫盒子
嘗試

####管理力
一致性
遵循原則
避免意外

1. PM = 團隊的 API
2. 協助團隊看到全貌以便規劃調度
3. 統一方向與做事方法

####總結
專案管理幫忙聚焦  
最小戰鬥單位的概念

### whoscall & mongodb

講者是 whoscall cto  
使用 mongodb 的經驗

#### What does Gogolook do?
Line whoscall  
Caller-ID Service  
介紹一下 mongodb 的基本性能
1. mongos
2. config server
3. mongod

#### issue

0th gae -> aws  
Pass to laaS  
No operation issue in GAE  
MongoDB Production Notes  
Nginx + AWS Auto-Scalling  

The 1st issue  
Page Faults 很高  
Index are in Memorry    
需要大量的 Memory  
刪除沒必要的 index  
升級 instance (scale-up)  

The 2nd issue  
資料量變大導致 DiskIO 問題  
需要更改 AWS 的設定  

The 3rd issue  
Lock rate 提高  
MongoDB concurrency  
一個 DB 只放 一個 collection  
其他方案
非即時需要丟到 Queue 處理  
等 MongoDB 更新 document-lock的功能  

The 4th issue  
shard 間資料希望能平均  
由 config server 控制   
三台 config server 之間的時間差異導致 balance 掛點因而loading 不平均。  
v2.6 可以 set time  
shard 時間不同步會導致交易時間不一致  
Object id 有使用到 timestamp 產生資料
因此如果將時間調到過去的時間會導致 Object id 碰撞的問題 

Conclusion

1. Index size fit in Memory
2. Disk IO
3. Database as Collection (< 2.8)
4. Time sync distributed system

你還會選擇 MongoDB嗎?
Redis 
elestic Search

災後還原的方案


### PHP Extension 開發實務 - 補齊 PHP 遺失的 $_PUT 與 $_DELETE (FirchTsai)

介紹一下 RESTful 
$_PUT  
$_DELETE  
違反了 RFC 2616 不應該實作到 PHP裡  
php://input  
處理 mulipart 

RFC 2388 mulipart 是什麼?

別忘了 $_FILES

EPV 

介紹Extension 的優點和架構  
主要是 SAPI 讓 server 與 php 溝通

1. 官方 Zend Extension API  
2. 神秘版 Zend Extension API (for PHP4) 用來來知道有這個 API
3. 終極版 Zend Extension API == 直接看原始碼

API 文件說明極少

PHP_GINIT_FUNCTION
PHP_GSHUTDOWN_FUNCTION

PHP_MINIT_FUNCTION
PHP_MSHUTDOWN_FUNCTION

PHP_RINIT_FUNCTION
PHP_RSHUTDOWN_FUNCTION

PHP-FPM 直接將 model 掛載到身上因此不會多次呼叫 init 和 shutdown。

config.m4 編譯環境  
config.w32  

php_epv.h 標頭檔  
epc.c 主要檔案  

編譯工具
1. phpize
2. configure
3. make
 
### Phalcon 進行式 (SDpower)

Phalcon Developer Tools  
講一些Phalcon 基礎大部分都用過了
快速使用加密解密  
不可逆加密  
都是在 service.php 設定  

### Building Powerful command-line application with PHP (c9s)

主要是介紹 [CLIFramework]
Features  
參考 GIT 的命令架構  

可以研究一下 zsh

[CLIFramework]:https://github.com/c9s/CLIFramework
### 實戰 HHVM Extension (Ricky)

介紹 HHVM

Hack lang = 強型態的 PHP
官方的文件
goo.gl/PPB64m

HHVM Extension requirement

config.cmake

fibionacci.php

hphpize
cmake
make && make install

PHP檔案只能有一個並且要用 ext 開頭

HNI(HHVM Native Interface)
讓 Hack 和 C++ 混用
類型互相對應

RTFSC == Read The Fxck Source Code
HHVM 密技  
JIT::VMRegAnchor






























