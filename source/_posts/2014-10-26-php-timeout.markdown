---
layout: post
title: "控制 PHP 執行時間"
date: 2014-10-26 13:38:11 +0800
comments: true
categories: ["php"]
---

如何控制 PHP 的最長執行時間。

<!-- more -->

在執行 PHP 腳本的時候有可能因為程式邏輯上的問題或是為了取得外部的資料導致執行時間過久，而讓使用者等待回應的時間過長帶來不好的體驗，
因此在 PHP 本身一些常用的函式庫或是伺服器設定會讓開發者設定 timeout 的時間。


#### nginx 
1. fastcgi_connect_timeout
2. fastcgi_send_timeout
3. fastcgi_read_timeout

#### php-fpm
1. php-fpm.conf 的 request_terminate_timeout

max_execution_time 和 set_time_limit 也能限制腳本執行的時間但是似乎在某些場景是有問題的。

#### curl
1. CURLOPT_TIMEOUT
2. CURLOPT_TIMEOUT_MS
3. CURLOPT_CONNECTTIMEOUT
4. CURLOPT_CONNECTTIMEOUT_MS
5. CURLOPT_DNS_CACHE_TIMEOUT

#### mysql
1. innodb_lock_wait_timeout
2. libmysql 的 MYSQL_OPT_READ_TIMEOUT 和 MYSQL_OPT_WRITE_TIMEOUT

#### memcached
1. bool Memcache::connect ( string $host [, int $port [, int $timeout ]] )
2. Memcached 要另外實現

#### redis
1. $redis->connect('127.0.0.1', 6379, 2.5); // 2.5 sec timeout.
2. $redis->pconnect('127.0.0.1', 6379, 2.5, 'x'); // x is sent as persistent_id and would be another connection the the three before.


#### 其他