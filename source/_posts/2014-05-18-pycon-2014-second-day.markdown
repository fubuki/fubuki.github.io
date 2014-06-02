---
layout: post
title: "Pycon 2014 second day"
date: 2014-05-18 19:30:24 +0800
comments: true
categories: ["open source"]
---

記錄一下Pycon 2014第二天(5/18)參加的議程
<!-- more -->

###Keynote: Jessica McKellar 
在世界各地從海底到太空都有人使用到python

data.goc.uk

KLP

python on windows

python on mobile

Can I build mobile apps in python 

kivy 

程式語言排行 

PyPL

說到 emscripten asm.js nodejs

Pythonjs skulpt brvthon  work with js

interactivepython.org

think in python

bnmentp/runestone github

PSF

PyLadies

Sprints

Grants rapberry pi

###What Is Async, How Does It Work, and When Should I Use It? 

pubsub pattern 

提到c10k問題 實現非同步的做法

前面大部分偷在講關於非同步的概念

1. twisted
2. tornado


後面開始講 asyncio

Yes:
  
* slow backend  
* websockets  
* many connections

NO:  
  
* cpu-bound
* no async driver
* no async expertise


###Building a Knowledge Graph - the new search engine technology

介紹一下知識圖譜
利用dbpedia(struct data from wiki) 的資料，使用python處理資料在丟在solr裡面。

synonym SynonymFilterFactory

介紹solr本身有的搜尋類型

Data source

data.gov.tw

open api

###How to integrate Python into a Scala stack to build realtime predictive models 
異種語言平台
跟ML沒有太大的關係。

Fliptop machine learning

* mathout
* Weka
* Scikit-learn

Weka GPL

mathout有些演算法沒有完全實踐

所以使用Scikit-learn，所以就介紹怎麼讓Python跟Scala黏合。

####Jython
有些使用c寫成的python library就無法使用
JyNI
還是無法支援 Numpy

####Jepp
會一直創建 python 直譯器

####thrift

No scala generator
scrooge

auto load balance

####REST API 
bottle

Thrift v.s. REST


### Keynote: Stephen McDonald

主要在介紹作者寫的mezzanine專案

mezzanine manage cms system

mathspace.co
kou.io

cms > site

講者怎麼建立 mezzanine 
http://bit.ly/MezzBegins

1. constraints
2. simplicity
3. just django

bit.ly/MezzLego

bit.ly/MezzPackages


###以廣告品項為基礎的行動廣告推薦系統: 以 Python Hadoop Streaming 實作 

廣告投放平台

CTR
Click Through rate

Conversion Rate
maximize converstions


最後6分鐘才有重點

### Poster Session

後面兩場議程都沒去聽，跑去聽Poster session。

跟line的開發人員聊了不少關於line 的架構。  
另外看到[raft]這個演算法，似乎是為了處理分散式系統一致的問題，另外有聽到JGroups這個工具似乎跟zookeeper是用來
處理類似的東西。

[raft]:http://raftconsensus.github.io/

