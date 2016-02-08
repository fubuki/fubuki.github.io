---
layout: post
title: "更換 Lucene Kuromoji 使用的 dic"
date: 2015-08-29 22:37:25 +0800
comments: true
categories: ["lucene"]
---


<!-- more -->

Lucene 內部是使用 Kuromoji 對日本語做處理，而 Kuromoji 底層是使用 mecab 的  MeCab-IPADIC dictionary，
所以如果要加新詞其實可以透過 mecab 增加詞彙。

1. [mecab-ipadic-neologd]
2. [修正されたmecab-ipadic-neologdの辞書を、Lucene Kuromojiに適用してみる]
3. [mecabの辞書を自動コストで作成]
4. [IPA、NAIST、UniDic、JUMANの辞書実演比較]


[mecab-ipadic-neologd]:https://github.com/neologd/mecab-ipadic-neologd
[修正されたmecab-ipadic-neologdの辞書を、Lucene Kuromojiに適用してみる]:http://d.hatena.ne.jp/Kazuhira/20150316/1426520209
[mecabの辞書を自動コストで作成]:http://qiita.com/wakisuke/items/d15b5defc1aad61cc910
[IPA、NAIST、UniDic、JUMANの辞書実演比較]:http://www.mwsoft.jp/programming/munou/mecab_dic_perform.html