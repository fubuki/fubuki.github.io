---
layout: post
title: "solr with mongo-connector"
date: 2014-04-19 15:51:14 +0800
comments: true
categories: ["solr"]
---

solr是一款開源的搜尋引擎，可以對各種資料索引，之前使用solr的Data-Import-Handler功能對Mysql作搜尋然後設定排程
定期將mysql資料丟到solr裡面，另外也有透過Mysql trigger和udf讓一些需要即時同步的資料。
<!-- more -->

solr與Mysql通訊是透過jdbc抓取資料庫裡的資料，而mongodb似乎也有類似的東西例如[mongo-jdbc]和[JDBC Driver for MongoDB]，
[mongo-jdbc]網路有人使用過雖可以讓solr進行索引但是如果要跑增量索引就會出錯，[JDBC Driver for MongoDB]則沒看到有人使用在
solr上的心得，之後有時間在測試。

mongodb本身則有[mongo-connector]這個解法，主要是利用Mongodb的oplog(類似Mysql的binlog)會記錄repset之間的操作，如此一來
讓solr透過oplog就可以去更新索引並且由於oplog是即時的讓solr能更即時更新資料。

如果要使用[mongo-connector]首先要打開replset 產生oplog然後安裝mongo-connector，不過遇到一個奇妙的問題透過pip安裝後沒有直接
連結到bin下之後透過git安裝就沒有問題了，要使用replset很簡單，就把/etc/mongodb.conf下面這段設定打開，

	# in replica set configuration, specify the name of the replica set
	replSet = example
之後在mongodb的shell裡下rs.initiate()指令即可，本台mongodb就變成PRIMARY了這時也可以加入其他台mongodb作replication，不過本次
主要是要使用oplog讓solr導入資料製作索引就不需要加入其他台server了。

接下來將照著github上Usage With Solr的說明使用即可，另外似乎可以搭配tailable cursor做出solr即時更新索引，之後在測試看看先加上
其他中文分詞分析中文資料。


[mongo-jdbc]: https://github.com/erh/mongo-jdbc
[mongo-connector]: https://github.com/10gen-labs/mongo-connector
[JDBC Driver for MongoDB]: http://www.unityjdbc.com/mongojdbc/mongo_jdbc.php