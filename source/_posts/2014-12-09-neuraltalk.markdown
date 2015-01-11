---
layout: post
title: "NeuralTalk : 從圖片生成文字描述的工具"
date: 2014-12-09 02:31:01 +0800
comments: true
categories: ["deep learning"]
---


<!-- more -->

[NeuralTalk] 是相當有趣的工具，透過 `deep learning` 的方法可以將圖片的情境使用文字描述出來，
這邊有不少 [example] 可以看到運行的效果，在 Github 上面也放有原始碼可以自行下載測試效果。

裡面使用了下面幾種模型:

1. Vinyals et al. from Google (CNN + LSTM)
2. Karpathy and Fei-Fei from Stanford (CNN + RNN)



[NeuralTalk]:https://github.com/karpathy/neuraltalk
[example]:http://cs.stanford.edu/people/karpathy/deepimagesent/