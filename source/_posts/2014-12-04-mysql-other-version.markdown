---
layout: post
title: "mysql 兼容方案"
date: 2014-12-04 10:45:55 +0800
comments: true
categories: ["mysql"]
---

<!-- more -->

列出幾個相容於 mysql 的開源方案。

### Percona Mysql
[Percona] 出的版本，目前看到身邊的人大都是使用這家公司出版的 Mysql 建立商業環境，
而且從它的討論區可以學習到不少如何對 Mysql 除錯的訊息。

### MariaDB
[mariadb] 是 Mysql 的生父另外開發的版本，裡面多增加了 TokuDB 這個引擎，目前在國外看到有些人將資料庫從 Mysql 遷移到
MariaDB，是值得期待的產品。

### MySQL/Galera
[galeracluster] 只有在網路上聽過這個版本，在找跟 Mysql Cluster 方案時看到有人提到，不過身邊的人似乎沒有人在使用這個版本。


### WebScaleSQL
Google 和 Facebook、LinkedIn、Twitter 共同開發的版本，上述的公司都有處理巨量資料的需求，所以看起來應該會朝向處理巨量資料和
佈署大規獏資料叢集的方向發展，不過我記得 Google 有決定當 MariaDB 成熟後將內部的 Mysql 資料庫遷移到 MariaDB，所以 MariaDB 和 WebScaleSQL
兩者會有有不同發展方向跟應用場景。

### InnoSQL
[InnoSQL] 是網易開發的 Mysql 分支，在它的 Github 上有列出改變了哪些部分，這些應該都是基於
網易內部需要而修改的，也許可以透過那些特性思考一下網易是如何使用 Mysql 。



[InnoSQL]:https://github.com/NetEase/InnoSQL
[Percona]:http://www.percona.com/
[mariadb]:https://mariadb.org/
[galeracluster]:http://galeracluster.com/

