---
layout: post
title: "C 語言的巨集"
date: 2015-01-10 22:43:00 +0800
comments: true
categories: ["C"]
---

<!-- more -->

之前在研究 Phalcon 的語法時看到下面這種定義巨集的程式碼，跟以前直接用大括號寫成 Function 的方式不一樣，
後來在別人的網誌看到這兩種的差別，直接使用 Function 的區塊寫法如果沒有注意寫法在預編譯的時候展開可能導致錯誤。

	/** Get the current hash key without copying the hash key */
	#define PHALCON_GET_HKEY(var, hash, hash_position) \
		do { \
			PHALCON_INIT_NVAR_PNULL(var); \
			phalcon_get_current_key(&var, hash, &hash_position TSRMLS_CC); \
		} while (0)


