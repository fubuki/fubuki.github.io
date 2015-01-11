---
layout: post
title: "mysqldump 備份資料庫指令"
date: 2014-12-29 21:26:15 +0800
comments: true
categories: ["mysql"]
---

<!-- more -->

最近幫別人整理資料庫發現資料表的結構設計不當導致資料過多的時候效率變很差，原本更改資料表的結構
但是由於手上沒有 root 權限的帳號，資料庫也不能停機開啟 `safe mode`，所以只能先刪除資料。


目前 MySQL 資料庫最常用 [mysqldump] 備份，在 MySQL 官網有詳細的解說裡面有很多選項可以使用，但是
目前最常用到的選項是 `-single-transaction` 和 `-lock-all-tables`，`-single-transaction` 是在備份
資料前開啟交易，讓資料能夠盡量完整匯出，而 `-lock-all-tables` 則是給 MyISAM 這類不支援 transaction
 的資料表所用，他會在備份時 Lock Table 為 READ LOCAL 狀態，只允許 [Concurrent Inserts]。




[mysqldump]:http://dev.mysql.com/doc/refman/5.1/en/mysqldump.html
[Concurrent Inserts]:http://dev.mysql.com/doc/refman/5.0/en/concurrent-inserts.html
[Percona XtraBackup]:http://www.percona.com/software/percona-xtrabackup