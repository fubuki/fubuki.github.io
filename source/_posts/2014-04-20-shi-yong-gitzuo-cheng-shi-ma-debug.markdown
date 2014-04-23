---
layout: post
title: "使用git做程式碼debug"
date: 2014-04-20 17:02:31 +0800
comments: true
categories: ["git"]
---

專案在多人協作的環境下有時會出現不明原因的bug，通常是因為撰寫的人沒有發現並且沒有經過良好的測試並且又併入主分支，
這導致bug隱藏在程式碼裡面，這邊就記錄一下平常使用git來找出問題點的方法。
<!-- more -->
通常如果知道出錯在哪個檔案可以透過git blame的指令找出此檔案最後修改的人是誰並且還可以得知最後的commit，並且還能夠
下條件限定在某些行數，下面的指令可以顯示 index.php 100行到150行之間的資訊另外我看可以下 `-C` 的選項可以顯示這段
程式碼的原始出處不過我一般沒有在使用。

		git blame -L 100,150 index.php

另外一種情形是不知道問題是出錯在哪一個部分，這時可以使用`git bisect`，這個指令可以讓使用者決定從哪邊開始是運作良好
的commit，然後現在是有問題的commit，接下來會顯示從正常到有問題的commit之間還有多少筆commit並且開一個`no branch`的
分支使用者讓測試，如果目前的commit是測試出來是正常的狀態便可以下`git bisect good`告訴 bisect目前的commit是正確的，
如果是錯誤的就可以下`git bisect bad`說目前是錯誤的狀態，直到確定是在哪一筆commit出錯的，結束後下`git bisect reset`
就可以回到原本的開發環境。

		git bisect start 開始執行bisect
		git bisect bad   目前的commit是有問題的
		git bisect good [commit] 目前已知的正常狀態是哪一個commit
		git bisect reset 結束 bisect