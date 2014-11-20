---
layout: post
title: "PHP One-Time Passwords"
date: 2014-11-10 22:02:49 +0800
comments: true
categories: ["php"]
---

使用 PHP 實現 One-Time Passwords (OTP) 。

<!-- more -->


### 什麼是 OTP
OTP 簡單說是每次使用帳密登入都是使用密碼產生器產生一次性密碼，這樣比起傳統的密碼安全許多，
但是需要額外裝置建構這個系統，目前似乎有人使用 email 和 sms 驗證。


### RFC 文件
1. [RFC 2289]
2. [RFC 1760]
3. [RFC 4226]
4. [RFC 6238]


### 相關專案
1. [PHP One-Time Passwords]
2. [oath-php]
3. [Mobile-OTP]

[PHP One-Time Passwords]:http://sourceforge.net/projects/php-otp/
[oath-php]:https://github.com/rbakels/oath-php
[Mobile-OTP]:http://motp.sourceforge.net/
[RFC 2289]:http://tools.ietf.org/html/rfc2289
[RFC 1760]:http://tools.ietf.org/html/rfc1760
[RFC 4226]:http://tools.ietf.org/html/rfc4226
[RFC 6238]:http://tools.ietf.org/html/rfc6238