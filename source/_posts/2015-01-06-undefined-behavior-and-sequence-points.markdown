---
layout: post
title: "Undefined Behavior and Sequence Points"
date: 2015-01-06 23:27:19 +0800
comments: true
categories: ["C++"]
---

<!-- more -->


今天在看編譯原理的書時看到了 [Undefined Behavior and Sequence Points] ，這兩個跟編譯器實作有關，通常在寫程式的時候應該是不會寫出有 `Undefined Behavior` 的片段，而 `Sequence Points` 跟 `side affetct` 比較有關。

`Undefined Behavior` 簡單說是有些程式碼由於在標準( ex: C++11)裡面沒有定義會輸出怎樣的結果，所以便會交給 Compiler 的開發者自行
實作，導致這類的程式碼會有不可預期的結果。

`Sequence Points` 是程式執行到某一個點時，前面的 `side affetct` 已經結束，後面的 `side affetct` 還沒有開始。


[Undefined Behavior and Sequence Points]:http://stackoverflow.com/questions/4176328/undefined-behavior-and-sequence-points