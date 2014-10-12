---
layout: post
title: "mariadb and tokudb"
date: 2014-09-05 23:49:44 +0800
comments: true
categories: ["mariadb"]
---

<!-- more -->


最近把虛擬機器上面的 MySQL 轉換成 MariaDB 兩者使用上沒有什麼不同，不過在 MariaDB 的官網上
看到一個沒見過的 TokuDB，查詢之後發現是新的儲存引擎並且也可以用在 MySQL上面，以前主要是使用
InnoDB， 可以比較一下兩者的優缺點也許在設計架構上可以有另外一種選擇。


參考資料 

1. [getting-to-know-tokudb-for-mysql]
2. github 上的源碼

[getting-to-know-tokudb-for-mysql]:http://www.percona.com/blog/2014/06/23/getting-to-know-tokudb-for-mysql/
[源碼]:https://github.com/Tokutek/tokudb-engine