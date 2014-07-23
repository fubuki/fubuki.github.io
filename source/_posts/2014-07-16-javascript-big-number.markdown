---
layout: post
title: "javascript big number"
date: 2014-07-16 21:06:32 +0800
comments: true
categories: ["javascript"]
---

關於在javascript裡面處理大數字的問題。
<!-- more -->

在javascript所有的數字類型都是以double的方式實現的，普通的時候是夠用的不過有時會遇到問題，起因是PHP輸出json格式的字串給閱覽器然後使用javascript解析時，解析完的資料含有超過18位元數字，導致由於精度下降的錯誤結果，然後在PHP裡面沒有錯的原因是他使用String的格式存放但在輸出json格式的時候使用了`JSON_NUMERIC_CHECK`的參數導致所有的內含數字的字串全都變成數字類型輸出。

之後我查看了JSON.stringify但是沒有參數可以處理這樣的問題，原本想自己寫一個處理JSON字串裡面有特大數字的函式庫，不過網路上已經有類似的函式庫可以使用，在此記錄一下，我是使用[json-bigint]去處理其他兩個是在找尋函式庫的時候找到的，不過只有第一個似乎比較符合我的需求。


1. [json-bigint]
2. [big.js]
3. [bignumber.js] 


[json-bigint]:https://github.com/sidorares/json-bigint
[big.js]:https://github.com/MikeMcl/big.js/
[bignumber.js]:https://github.com/MikeMcl/bignumber.js/