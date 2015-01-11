---
layout: post
title: "分散式檔案系統"
date: 2014-12-11 22:50:42 +0800
comments: true
categories: ["distributed system"]
---

紀錄一下目前有看過哪些分散式檔案系統。

<!-- more -->

在以前 Google 內部使用自行開發的 GFS 作為檔案系統，並且將相關論文開放給外界參考後生出了 hadoop 之類的軟體，
而現在有不少生產環境使用了分散式檔案系統，

1. HDFS
2. LeoFS
3. MogileFS
4. ZFS
5. FastDFS
6. GlusterFS
7. GridFS
8. TFS

### HDFS
hadoop 所使用的檔案系統。

### LeoFS
以前同事待的公司使用 DFS 系統。

### MogileFS
KKBOX 內部使用 MogileFS 存放音樂資料。

### ZFS
由 SUN 所開發檔案系統，一開始是在 Solaris 才有的後來有人移植到各種作業系統上。

### FastDFS
[fastdfs]:https://code.google.com/p/fastdfs/

### GlusterFS
目前似乎由 Red Hat 維護。

### GridFS
MongoDB  使用的一種檔案系統。

### TFS
淘寶開發的檔案系統。