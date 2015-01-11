---
layout: post
title: "Docker 的 Storage Driver"
date: 2014-12-23 21:46:07 +0800
comments: true
categories: ["docker"]
---

最近似乎是因為 docker 的 Storage Driver 關係導致 Kernel Bug 所以要研究一下這一個部分。

<!-- more -->

如果在命令列下 `docker -D info` 其中就可以看到目前機器上的 Storage Driver 是什麼，目前我手上兩種 Linux 發行版， 
在 ubuntu 14.04LTS 下可以看是 `aufs`，如果是在 centos 6 會是 `device-mapper`，另外 docker 還有支援 Btrfs。


####　Aufs
目前只有在 Debain 系列的 Linux 版本才有包進內核裡的檔案系統，開發者是名叫`岡島順治郎`的日本人，從網路上的評價
來看 Aufs 似乎是個蠻不錯的檔案系統，但是由於一些原因一直不能加進 Linux 的內核裡面，原因似乎是代碼寫的不太好的原因。


官網在這 [Aufs] 另有一些可以研究的東西 `Union mount` 和 `UnionFS`.


[Aufs]:http://aufs.sourceforge.net/

#### Device-mapper

[Linux 内核中的 Device Mapper 機制]

[Linux 内核中的 Device Mapper 機制]:http://www.ibm.com/developerworks/cn/linux/l-devmapper/index.html

#### Btrfs

Oracle 開發的檔案系統，從 2007 年開始開發，已經有穩定版可以使用，目前 facebook 有在測試這個檔案系統。

wiki : [btrfs]

[btrfs]:https://btrfs.wiki.kernel.org/index.php/Main_Page



