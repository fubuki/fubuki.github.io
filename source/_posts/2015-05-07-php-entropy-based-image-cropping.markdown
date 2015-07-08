---
layout: post
title: "PHP entropy based image cropping"
date: 2015-05-07 22:29:00 +0800
comments: true
categories: [""]
---


<!-- more -->


以前在做圖片上傳網站時需要對圖片做 crop 和 resize，但是要對圖片作 crop 需要決定要怎麼處理
才能保留重要的部分，最初是選擇圖片的中央部分，後來有想過使用邊緣檢測和特徵檢測得出需要的部分，
後來看到一個使用 Entropy 的方法，在 [crop] 裡面有實作的方法，在 [Cropping Images in PHP Based on their Entropy] 
裡面有不少相關的討論可以參考。





[Cropping Images in PHP Based on their Entropy]:http://www.reddit.com/r/programming/comments/1wz2e4/cropping_images_in_php_based_on_their_entropy/
[crop]:https://github.com/stojg/crop