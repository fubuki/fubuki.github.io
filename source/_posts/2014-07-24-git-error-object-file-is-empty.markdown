---
layout: post
title: "git error object file is empty"
date: 2014-07-24 21:48:08 +0800
comments: true
categories: ["git"]
---

<!-- more -->

昨天在使用 git 的時候發生了一件怪事，在 commit 的時候顯示下面的錯誤訊息，似乎是專案本身 git 的資訊出錯了，導致所以
整個專案都有問題了，由於專案在github 上面有備份所以就直接 clone 一份下來，不過似乎是可以修好的。 

		
error: object file .git/objects/7e/b04b2f04cd57e890b010a465c755249ee57f27 is empty
fatal: loose object 7eb04b2f04cd57e890b010a465c755249ee57f27 (stored in .git/objects/7e/b04b2f04cd57e890b010a465c755249ee57f27) is corrupt


[how to fix GIT error: object file is empty?] 這篇文章有提到怎麼修復，如果有在遇到相同的問題可以嘗試看看。


[how to fix GIT error: object file is empty?]: http://stackoverflow.com/questions/11706215/how-to-fix-git-error-object-file-is-empty
