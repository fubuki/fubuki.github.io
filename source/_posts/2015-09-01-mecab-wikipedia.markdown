---
layout: post
title: "Mecab 使用 Wikipedia 增加詞庫"
date: 2015-09-01 23:36:16 +0800
comments: true
categories: ["nlp"]
---

<!-- more -->


Mecab 可以自行增加詞庫的內容，增加的內容從目前看到的資料有幾個可以使用，主要是要轉換成
Mecab 可以吃的格式。

### 可以使用的資料來源

1. Wikipedia jp
2. NicoNico
3. hatenaキーワード

### 轉換方法

1. 安裝 icu 工具用來轉換文字編碼。
2. 將輸入資料轉換成 csv 格式
3. 使用 `mecab-dict-index` 將 csv 檔案轉換成 dic 檔案


### 問題
轉換時要注意跟 system dic 的編碼要相同不然會發生錯誤。

	CHECK_CLOSE_FALSE(sysdic->isCompatible(*d)) << "incompatible dictionary: "  

	context_id.cpp(88) [it != left_.end()] cannot find LEFT-

另外有個問題使用這樣的方式匯入的詞是沒有讀音的要另外想辦法輸入。