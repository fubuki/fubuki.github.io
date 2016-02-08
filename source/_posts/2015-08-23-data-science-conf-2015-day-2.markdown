---
layout: post
title: "資料科學年會 2015 Day 2"
date: 2015-08-23 22:00:07 +0800
comments: true
categories: ["conference"]
---

<!-- more -->

### Big Education in the Era of Big Data 

Collective Probabilistic Model

我們的教育體制

第一個大資料挑戰 人口普查

講一些泛用的資料處理步驟

資料分析在教育上的應用

Top 10 elearning Statistics

一些線上教育平台

學習精神

MOOCs




### 從網頁存取記錄瞭解使用者行為與網頁區塊貢獻分析-實戰篇

從 access_log 研究 Data driven


log 處理速度

####頁面板塊分析
必須先統計每個板塊的點擊狀況
統計方式
1. redirect
2. 增加 ref 參數
3. 

ref 帶有的資訊
正在哪一頁的哪個版塊和相關資訊

Ref v.1 
Ref v.2   如果網站結構改了會有問題吧
Ref v.3

他們有做線上 ABtest?

Google 搜尋 SEO 會有問題

#### 開始處理 web access log

為了彌補 GA 沒有的功能

爬蟲很多所以需要過濾


有些必須另外蒐集的資料

這邊使用 Kafka 處理 web access log

clickstream ????

Ref 應該可以完成之前想玩了使用者行為追蹤

強化自己的全文搜尋??? 強化斷詞關係

Ref 的好處

處理 Kafka 

Log 儲存 Impala + sql like , PostgreSQL

程式語言 Java

資料整理Excel + Java


RWD 版型怎麼辦 利用 javascript 偵測

跳出率 沒被點擊物品 搜尋優化

### 使用 Elasticsearch 及 Kibana 進行巨量資料搜尋及視覺化

巨量資料怎麼 LOG

資料都是從 mongodb 上匯入的 那會匯入的方式是?

介紹一些內建的資料處理和視覺化方法，果能夠將 access log 匯入
就可以建立一個簡單的監控系統

這邊提到了 Hyperloglog 和 Percentile*  T-digest

gogolook 架構 使用 fluentd 

未來可能增加停留時間的記錄

Logstash 比較沒有人在開發所以建議使用 fluentd

### Visualiztion over Web Tools and Tips

Apple device resolutioins

這邊都是再說 RWD 的設計

不過這邊應該有更多可以考慮的方式

SVG preserveApsectRatio

網頁設計講比較多，因為是要讓資料顯示在網頁上

ai2html

繪圖優化

Cross Device

有些有趣的網站可以參考

### 團結力量大？集團企業之解構、分析比較

這邊主要是利用投資的相關資料畫出相關性。


### 社會資訊學？資訊社會學？抑都不是？淺論資訊科學與社會學相得益彰的合作契機

計算社會學

社會學內容

Agent Based Modeling

資訊科技在社會科學上的應用

有些社會學上的大哉問


### gov

1. 分析蘋果日報的留言 可以看看
2. 判決書非常非常長 
3. 新聞品質 量化分析
4. 血庫存量
5. 新台語 運動 台語字典
6. Data Design 
7. IoT 空汙偵測 DIY
8. etc

詞頻分析

後面有一系列資料，有些可以研究研究