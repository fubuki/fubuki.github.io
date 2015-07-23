---
layout: post
title: "browser reflow repaint"
date: 2015-07-08 20:47:58 +0800
comments: true
categories: ["frontend"]
---

<!-- more -->

### reflow
重排整個瀏覽器的元素，例如當有元素的寬高改變的時候需要將整個 DOM 重新計算。

### repaint
對單一元素重繪，例如更改字體大小或是顏色。


1. [Minimizing browser reflow]
2. [Reflows & Repaints: CSS Performance making your JavaScript slow?]

[Minimizing browser reflow]:https://developers.google.com/speed/articles/reflow
[Reflows & Repaints: CSS Performance making your JavaScript slow?]:http://www.stubbornella.org/content/2009/03/27/reflows-repaints-css-performance-making-your-javascript-slow/