---
layout: post
title: "Facebook login JavaScript SDK 在 webview下的問題"
date: 2014-06-06 22:31:54 +0800
comments: true
categories: ["frontend"]
---
在android或是ios底下使用Facebook 的JavaScript SDK通常是透過webview之類的實作，但是在需要登入Facebook的時候
，雖然會導向登入頁但是卻無法正常導回登入前的頁面，畫面會呈現一片空白，後來發現有可能是因為Facebook是用popout
出一個登入頁使得登入完成後無法正常redirect導原本的頁面才會發生這種情形，網路上有些解法是更改webview部分的程式碼
讓redirect可以正常運作，不過還有另外一個方法是使用javascript直接導向facebook手機板的登入頁在redirect回來便可以
避免登入後會出現空白頁的問題。