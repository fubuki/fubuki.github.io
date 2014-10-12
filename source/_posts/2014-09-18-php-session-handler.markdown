---
layout: post
title: "PHP session handler"
date: 2014-09-18 23:16:14 +0800
comments: true
categories: ["php"]
---

<!-- more -->


之前在使用 node.js 搭建 WEB 聊天伺服器的時候，需要跟 PHP 端共用 session ，當時是使用 memcached 儲存 session 資訊，
但是預設是使用 PHP 的序列化格式，所以換成 msgpack 和 igbinary 兩種格式測試，使用 `session_set_save_handler` 實現，
如此一來透過 memcached 分享兩個平台的認證資訊。