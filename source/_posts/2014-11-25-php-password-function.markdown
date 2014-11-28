---
layout: post
title: "PHP 5.5 的 Password Function"
date: 2014-11-25 21:57:54 +0800
comments: true
categories: ["php"]
---

<!-- more -->

PHP 5.5 新加了用來處理 Password 加密的功能，[Password Hashing Functions] 裡面有列出新增的四個 function。

### password_get_info
傳入一個加密字串取得。

### password_hash
針對一個字串加密。

### password_needs_rehash
當加密字串遺失了一些資訊時可以透過這個重新加密字串。

### password_verify
確認字串和加密後的 hash 是否相同。


### 相關資訊
[PHP RFC: password_hash() function behavior]
[Request for Comments: Adding simple password hashing API]

[Password Hashing Functions]:http://php.net/manual/en/ref.password.php
[PHP RFC: password_hash() function behavior]:https://wiki.php.net/rfc/password_hash_spec
[Request for Comments: Adding simple password hashing API]:https://wiki.php.net/rfc/password_hash