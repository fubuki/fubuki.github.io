---
layout: post
title: "圍棋的UCT演算法"
date: 2014-07-29 23:03:06 +0800
comments: true
categories: ["algorithm"]
---

在搜尋關於使用統計方法處理自然語言的時候意外看到的東西。

<!-- more -->

以前在大學在上關於人工智慧的課程有提到比起象棋、西洋棋，製作圍棋的人工智慧更困難，
由於可能下的步數太多了導致複雜度比起上述的棋類遊戲還難製作。

到了現在意外看到了UCT演算法，似乎是基於蒙地卡羅法的樹狀搜尋演算法，詳細內容可以參照
[Monte-Carlo_tree_search]或是[Monte_Carlo_Tree_Search]，看起來主要是用了Upper Confidence Bounds (UCB)，如果要真正理解就要需要實作一次了。


附註 UCB 演算法 Multi-armed Bandit，   Bandit Algorithms for Website Optimization


[Monte-Carlo_tree_search]:http://en.wikipedia.org/wiki/Monte-Carlo_tree_search
[Monte_Carlo_Tree_Search]:http://www.game.csie.ndhu.edu.tw/gamewiki/index.php/Monte_Carlo_Tree_Search



[BanditsBook]:https://github.com/johnmyleswhite/BanditsBook