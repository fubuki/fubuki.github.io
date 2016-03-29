---
layout: post
title: "python https error"
date: 2016-03-13 23:06:56 +0800
comments: true
categories: ["python"]
---

<!-- more -->



因為 python  版本比較舊在使用 urlib3 時處理 SSL 的連結會出問題，解決方法一個是升級，
另外一個使用 [SNIMissingWarning] 的方法解決。


[SNIMissingWarning]:https://urllib3.readthedocs.org/en/latest/security.html#snimissingwarning