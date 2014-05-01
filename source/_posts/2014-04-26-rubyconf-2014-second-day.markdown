---
layout: post
title: "rubyconf 2014 second day"
date: 2014-04-26 20:29:49 +0800
comments: true
categories: ['open source']
---

記錄一下rubyconf 2014第二天(4/26)參加的議程
<!-- more -->

### Cores unleashed - Exploiting Parallelism in Ruby with STM (and a new VM)  
[slide]  

### How the Principles of Ruby Inspired the Rails Girls Community
兩位講者如何認識，並且介紹Rails Girls社群怎麼成長的。

### Ruby on Bioinformatics
使用ruby 處理生物資訊，列了不少gem但是有的是去使用其他語言的library吧，裡面也有提到使用neo4j處理
個人的健康資料，不過跟ruby沒有太大的關係，現在比較常用還是perl和python吧。

### the Guide to know Ruby implementation for non-C language programer
講者一開始說因為她的先生是寫ruby的programmer接觸ruby，之後就開始研究Ruby裡面的架構，
講者介紹幾個方法去研究裡面的原始碼。


### Growing Up - Bringing Concurrency to Ruby
一開始介紹jruby和jvm，然後說明 prcoess-level和thread-level的做法，concurency的法則和
實現介紹一些實現no-block的library。


### Extreme Makeover - Rubygems Edition
bundle，用來管理gem的依賴性，講者講了一些過去bundle的issue，ssl issue，搜尋Gem的效率過低，加上CDN，
加入一些api，建立新的index。


### sweaters as a service - adventures in electronic knitting
講者建立一個編織機器，只要上傳圖檔就可以編織出一個圖案，似乎是使用Ruby去控制不過沒有看到整個程式碼。


### Improve and refactor ruby code easier
利用 synvert工具作ruby 的重構。


### lightning talk



[slide]: https://speakerdeck.com/brucehsu/rubyconf-dot-tw-2014-cores-unleashed-exploiting-parallelism-in-ruby-with-stm