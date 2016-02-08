---
layout: post
title: "elasticsearch autocomplete 功能"
date: 2015-08-28 21:54:13 +0800
comments: true
categories: ["elasticsearch"]
---

<!-- more -->


elasticsearch 的 suggest 主要分成下面三種

1. Phrase Suggester
2. Term suggester
3. Completion Suggester


其中 `Completion Suggester` 目前看起來最適合用來實做 autocomplete 功能，使用上可以搭配  `category` 可以
增強 autocomplete 的功能，`category` 能夠自行添加欄位讓開發者可以對資料進行過濾。

目前看起來有幾點要注意:

1. Completion Suggester 可以透過加上 weight 調整排序。
2. Completion Suggester 有 input 和 output 的欄位，可以讓多個輸入對應到單一輸輸出。
3. 如果有多個 document 相同 output 那 elasticsearch 會只輸出一個。
4. Category 可以參照 [Elasticsearch 1.2: Adding Context to Suggestions] 裡面有個使用 Category 過濾的例子。
 

#### 建立 index 和 mapping file


#### 加入 document


#### 更新 document


#### 搜尋


[Elasticsearch 1.2: Adding Context to Suggestions]:https://www.elastic.co/blog/elasticsearch-1-2-adding-context-suggestions