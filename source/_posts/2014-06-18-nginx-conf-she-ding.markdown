---
layout: post
title: "nginx conf 設定"
date: 2014-06-18 22:56:40 +0800
comments: true
categories: ["nginx"]
---
記錄關於nginx 設定檔的配置。

<!-- more -->

## 分類
1. debug
2. 優化
3. 運行必備
4. 事件類型


## debug用
1. deamon
2. master_process
3. error_log
4. debug_points
5. debug_connection
6. worker_rlimit_core
7. working_directory

## 優化
1. worker_processes
2. worker_cpu_affinity
3. ssl_engine
4. timer_resolution
5. worker_priority

## 運行必備
1. env 環境變數
2. include
3. pid file
4. user 
5. worker_rlimit_nofile

## 事件類型
1. accept_mutex
2. lock_file
3. accept_mutex_dely
4. multi_accept
5. use epoll
6. worker_connections
