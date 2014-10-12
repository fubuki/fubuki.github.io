---
layout: post
title: "node.js and php-fpm"
date: 2014-09-21 22:01:45 +0800
comments: true
categories: ["nodejs"]
---

php-fpm 實現 fast-cgi 的規格來處理 php script，而 node.js 就可以透過 fast-cgi 執行跟 php-fpm 通信執行 php script。

<!-- more -->

網路上有一些已經時間 node.js 跟 fast-cgi 通信的 library，不過都有點舊，之前有實際跑了一下會有些問題，不過大致上
從別人寫的 library 和 [FastCGI Specification] 可以了解 fast-cgi 的通信接口，之後可以自己玩玩看。

[fast-cgi]:http://www.fastcgi.com/drupal/
[FastCGI Specification]:http://www.fastcgi.com/drupal/node/6?q=node/22