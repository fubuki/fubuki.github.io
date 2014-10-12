---
layout: post
title: "hippyvm and  hhvm"
date: 2014-09-12 22:54:48 +0800
comments: true
categories: ["php"]
---

<!-- more -->

以前在研究 Facebook架構的時候看到 `hhvm` 這個東西，把 PHP 編譯成二進位碼然後運行在虛擬機器上，
而最近又看到另外一款類似的產品 `hippyvm`，據說比 `hhvm` 還要快。


`hhvm` 是用 C 和 C++ 撰寫的，而 `hippyvm` 是用 pypy 撰寫的，不過兩者都是將 PHP 運行在自己的虛擬機器上，
也因此有些基於 zend engine 的插件應該無法直接使用，需要修改源碼才行，這也是當初沒有在工作上採用的原因，
而是使用 phalcon 跟 Zephir 開發專案。

目前在網路可以看到一些關於 hhvm 和 phalcon 之間比較的文章，兩者各有其優點，不過身旁看到的都是使用 phalcon 開發
來提高 PHP 的性能，反而沒看到使用 hhvm 的人，但是不管怎樣這兩者能夠共同發展對 PHP 也是件好事。

[hhvm]:http://hhvm.com/
[hippyvm]:http://hippyvm.com/