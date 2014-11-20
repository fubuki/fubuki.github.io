---
layout: post
title: "php 的加密方案"
date: 2014-10-14 22:09:47 +0800
comments: true
categories: ["php"]
---

<!-- more -->

最近需要生成一些加密字串，需要研究一下要採用哪種加密演算法， md5 跟 sha1 應該是不會列入考慮， 有可能會在 bcrypt 和 scrypt 兩者之間比較
一下看是要選擇哪一個。

1. crypt 
2. bcrypt 
3. scrypt


#### 關於加密的文章
[How to securely hash passwords?]
[Secure hash and salt for PHP passwords]


[How to securely hash passwords?]: http://security.stackexchange.com/questions/211/how-to-securely-hash-passwords/31846#31846
[Secure hash and salt for PHP passwords]: http://stackoverflow.com/questions/401656/secure-hash-and-salt-for-php-passwords/8050063