---
layout: post
title: "中文分詞器"
date: 2014-04-15 20:55:40 +0800
comments: true
categories: ["NLP"]
---

記錄一下中文分詞目前有哪些分詞並且主要使用哪些方法實現中文分詞。
<!-- more -->
目前有哪些中文分詞器。  
1. [IKAnalyzer]  
2. [mmseg4j]  
3. [paoding]  
4. [ansj_seg]

中文分詞比較常見的是使用詞典進行分詞，使用這種方法最重要是詞典的內容，通常利用輸入法或是網路上放出來的詞典，不過有些新詞或是人名地名
就沒有辦法處理，另外一點就在分詞速率，透過詞典分詞詞典越大分詞的時間就會越久。另外是使用機器學習透過語料庫訓練出模型例如HMM的方式也是
需要透過既有的語料庫訓練。此外也能夠使用語言學上的規則方法不過我目前看到的分詞器大多都是詞典加統計模型。


[IKAnalyzer]: http://code.google.com/p/ik-analyzer/
[mmseg4j]: https://code.google.com/p/mmseg4j/
[paoding]: https://code.google.com/p/paoding/
[ansj_seg]: https://github.com/fubuki/ansj_seg
