---
layout: post
title: "Oracle 1000 in clause limit"
date: 2014-07-21 23:57:50 +0800
comments: true
categories: 
---

關於 ORA-01795的錯誤。
<!-- more -->

在 oracle 使用 where in 的條件語句下遇到了一個問題，oracle 在使用超過1000個的 elemet會跳`ORA-01795`錯誤，
在網路上有不少解法，下面會記錄一下有哪些解法，不過由於工作上是使用phalcon 如果要使用網路上的解法就要轉用 `raw sql`
的方式讀取資料庫。