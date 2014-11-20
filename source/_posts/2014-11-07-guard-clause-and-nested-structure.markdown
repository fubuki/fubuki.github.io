---
layout: post
title: "guard clause and nested structure"
date: 2014-11-07 08:18:53 +0800
comments: true
categories: ["design pattern"]
---


<!-- more -->


在一個函數裡面通常會有多個 if else 的條件子句，這時會有下面兩種寫法。

### Guard Clause
Guard 有著防禦的意思，是在條件子句中直接離開函數，每個條件子句都是同一個階層。

	if (xxx) {
		return;
	}

	if (yyy) {
		return 
	}

	return;
### Nested Structure
在一個條件子句中還有多層的條件子句，因此會看到下面這種情形，導致之後別人維護會很難看懂整個程式的。
	
	if (x == 1) {
		// do something
		if(y == 3) {
			// do something
			if(x == 4) {
				// do something
			} else {
			
			}
		} else {
		
		}
	}

### 感想
大部分時候我都是用 Guard Clause 的寫法，我覺得盡量減少 `if else` 的層級看起來比較好懂也比較容易給之後的人維護修改，可以很容易看
出每個條件子句的用途為何。



