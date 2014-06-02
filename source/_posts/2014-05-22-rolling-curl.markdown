---
layout: post
title: "Rolling cURL"
date: 2014-05-22 22:51:01 +0800
comments: true
categories: ["php"]
---

cURL 是用來模擬各種http請求的工具，PHP也使用這個工具來取得網頁內容，或是呼叫一些API，
但是使用上會存在一些效能上的問題，如果只是單純呼叫cURL可能會阻塞住，就必須更加巧妙的去使用cURL。

<!-- more -->

[Rolling cURL: PHP并发最佳实践]這篇文章有提到兩種寫法，都是使用[curl_multi_exec]去實踐，但是實踐的
方法不太一樣可以仔細研究，在github上面也有些專案例如:[php-multi-curl]，可以看看裡面的原理，以提高
cURL並發下的效能。





[curl_multi_exec]: http://se2.php.net/manual/en/function.curl-multi-exec.php
[Rolling cURL: PHP并发最佳实践]: http://www.searchtb.com/2012/06/rolling-curl-best-practices.html
[php-multi-curl]: https://github.com/jmathai/php-multi-curl