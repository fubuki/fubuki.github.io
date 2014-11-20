---
layout: post
title: "PHP 使用 PDO 與 mysql 進行持久化連接"
date: 2014-11-06 21:58:49 +0800
comments: true
categories: ["mysql"]
---


<!-- more -->


在 PHP 裡面如果使用 PDO 連接 Mysql 有個 `PDO::ATTR_PERSISTENT` 的選項可以形成 `persistent connection`，其中的機制是在 PHP script 結束的時候將連線交由背後的進程管理，
如果是使用 fastcgi 就會由 fastcgi 負責管理，另外從 [php持久化连接数据库] 的測試結果不管是用 apachehandle 或是 php-fpm 都可以支援持久化連線。



在 [What are the disadvantages of using persistent connection in PDO] 裡面有提到一些持久化連線會導致的問題值得一看，另外在最近同事使用持久化連線的時候遇到了 `MySQL server has gone away`
的問題，似乎是 PHP 端的持久化連線已經 lost 掉跟 mysql 的連線了但是卻沒有在次跟 mysql  重新連線的關係。


[php持久化连接数据库]:http://eslizn.com/archives/39/
[What are the disadvantages of using persistent connection in PDO]:http://stackoverflow.com/questions/3332074/what-are-the-disadvantages-of-using-persistent-connection-in-pdo/5541150#5541150
[MySQL “Gone Away” Error with Persistent PHP Connection]:http://stackoverflow.com/questions/26620625/mysql-gone-away-error-with-persistent-php-connection