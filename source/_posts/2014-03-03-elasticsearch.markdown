---
layout: post
title: "elasticsearch"
date: 2014-03-03 21:51:01 +0800
comments: true
categories: ['search engine']
---

elasticsearch 另外一款搜尋引擎，之前就有在注意了，目前已經有出現1.0版本，  
不過底層跟solr都是lucene，使用上要去抓取資料庫的內容要另外設定，我比較中意
Solr只要將欄位設定好就可以直接使用。  
<!-- more -->

目前維基百科和github都用elasticsearch解決他們搜尋功能，不知道背後是如何運用的，  
這邊要使用了話主要問題還是在cjk分詞，之前是用詞典的方式，如果換用HMM或是n-gram的方式
來增加分詞的精確度是最要緊的。

