---
layout: post
title: "nginx upstream 反向代理的機制"
date: 2014-06-19 22:21:25 +0800
comments: true
categories: ["nginx"]
---

如何設定nginx 反向代理的功能。

<!-- more -->

##upstream 建立流程與機制
1. 啟動upstream
2. 與上游伺服器建立連結
3. 發送請求給上游伺服器
4. 接收上游伺服器的響應頭部
5. 轉發跟不轉發響應
6. 結束upstream的請求



##與upstream相關的原始碼
1. ngx_http_upstream_init  
2. ngx_http_upstream_init_request
