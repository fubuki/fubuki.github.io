---
layout: post
title: "在 apache 安裝上 wsgi 執行 django"
date: 2014-12-15 21:57:18 +0800
comments: true
categories: ["python"]
---

<!-- more -->

apache 上面可以藉由安裝 mod_wsgi 執行 python 的程式碼，這邊記錄一下在 Centos 上面的安裝過程。

Apache 和 python 一開始就安裝在機器上面了，然後 django 和 web.py 則是透過 `pip` 或是 `easy_install` 安裝,以為很簡單卻卡在安裝 mod_wsgi 上面。

原本是透過 [mod_wsgi] 的原始碼編譯，但是出現下面的錯誤:

	apxs:Error: Command failed with rc=65536

原因在官網的 [Installation Issues] 有提到是因為 python 和 apache 的版本不合，一個為 32 位元一個為 64 位元就會
出現這種錯誤，只能重新編譯。


後來試著用 `yum install mod_wsgi` 成功安裝但是在 apache 的 error log 出現 `ImportError: No module named web` ，
在 web.py 的官網建議加入檔案路徑加入環境變數，不過還是失敗。

最後發現是 python 版本的問題，機器上面安裝兩種 python 的版本 2.6 和 2.7， yum 透過 2.6 編譯 mod_wsgi 與程式使用的
 2.7 不同而導致這個問題，最後下載 python 原始碼重新編譯才行。

 下載 python 的原始碼並且在 configure 加上 --enable-shared 編譯安裝，安裝後執行 python 遇到下面的錯誤，找不到 lib 的路徑。

 	python: error while loading shared libraries: libpython2.7.so.1.0: cannot open shared object file: No such file or directory

使用 ldconfig 指定 lib 位置後重新編譯安裝 mode_wsgi 就建立好環境了。


[mod_wsgi]:https://code.google.com/p/modwsgi/
[Installation Issues]:https://code.google.com/p/modwsgi/wiki/InstallationIssues