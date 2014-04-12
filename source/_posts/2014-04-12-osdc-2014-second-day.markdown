---
layout: post
title: "OSDC 2014 second day"
date: 2014-04-12 19:20:57 +0800
comments: true
categories: 
---

記錄一下OSDC 2014第二天(4/12)參加的議程
<!-- more -->

### Minimal MVC in JavaScript
講者是Mosky，這場人爆滿，去年Pycon有聽過Mosky的議程，這場就簡單說一下什麼是MVC架構，
並且寫出一個簡單的MVC framework。

#####memo app
https://github.com/moskytw/memo-app/blob/master/memo/static/memo.js
#####ZipCodeTW
[repo] https://github.com/moskytw/zipcodetw  
[demo page] http://zipcode.mosky.tw/

### 當黃色小鴨都可以進入基隆，Node.js 當然也可以娶 QML
以前有用Qt寫過GUI的程式，QML是Wt放出來的語言，可以混用javascript不過支援的功能有限，為了擴充功能需要懂得C++才能擴展，原本講者在有弄一個nodejs+qt的函式庫<del>Brig</del> 不過後來就放棄了，之後講者找到一個[qtjs] == Node.js + Qt + API Generator，

講者弄個live demo是會顯示IRC頻道的內容的BOT不過似乎因為中文編碼的關係出現問題。

[qtjs]: https://github.com/svalaskevicius/qtjs-generator

### Data Visualization in D3js - Tips and Tricks
這場也是爆滿，講者一開始說本場議程會一一說明有哪些tips並且在後面用火焰顯示難度，最多是4個火焰，
第一個tip是purpose就四個火焰，丟出不少有趣的圖表，顯示出根據觀測的角度不同呈現出的東西就不一樣，後面的tips主要是跟別的專案結合並且要多看官網的範例，最後是demo一個使用  Angularjs + D3js fisheye + x3d的Banana 3D 。

### Escape from the Callback Hell
這場我以為是要講javascirpt，不過作者比較熟悉的python和 object-c不過也提到一些javascript，講了一些語言在處理callback非同步
的方式。

Objective-C block  
python 3.3的Coroutines  
C# async await  
nodejs 0.12 提供yield的功能  
[co]

[co]: https://www.npmjs.org/package/co

### Bashing OSDC
講者主要使用Bash和介紹Bash，上午有場同個講者是使用命令列管理Github的議程，然後有觀眾問了[fish]可以研究看看。  
講者的github:[ingydotnet]
[ingydotnet]: https://github.com/ingydotnet
[fish]: http://fishshell.com/
### 從 Multics 到雲端作業系統：淺談系統程式發展和新機會
jserv的議程，這場介紹從以前到現在作業系統的發展，從登月使用的CTSS到後在發展的multics unix bsd，並介紹他們各自實現的功能和概念，之後講了BeOS和NeXT和各自後來的發展。
'現在智慧型手機的市場其實是 Linux 跟 BSD 在比誰的 user experience 比較好'這句話蠻有趣的。
接下來開始說講者在生醫產業的發展和開發的F9 Microkernel。
自己的國家自己救->自己國家的教育自己救->自己的<del>老弟</del>醫療系統自己救。


### 零時政府的第一年
這場分成兩個部分。
第一部分是g0v是如何發展的，網路動員的窘境，有哪些專案。
第二部分是在"中研院"辦了第零次向日葵數位體驗營的過程和心得。

### Lightning Talks