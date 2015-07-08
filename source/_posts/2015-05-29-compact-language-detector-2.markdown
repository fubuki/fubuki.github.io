---
layout: post
title: "Compact Language Detector 2"
date: 2015-05-29 21:02:49 +0800
comments: true
categories: [""]
---

<!-- more -->

[Compact Language Detector 2] 是 chrome 用來偵測目前網頁的使用的語言，提示使用者可以翻譯成目前使用的語言，
從網站的說明看是用 `Naïve Bayesian classifier` ， 然後有三種資料集當作分類的分數。

### For Unicode scripts such as Greek and Thai that map one-to-one to detected languages, the script defines the result

### For the 80,000+ character Han script and its CJK combination with Hiragana, Katakana, and Hangul scripts, single letters (unigrams) are scored


### For all other scripts, sequences of four letters (quadgrams) are scored

[Compact Language Detector 2]:https://code.google.com/p/cld2/