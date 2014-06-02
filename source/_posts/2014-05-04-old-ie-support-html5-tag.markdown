---
layout: post
title: "Old IE Support Html5 Tag"
date: 2014-05-04 20:28:03 +0800
comments: true
categories: 
---

舊版本IE支援 html5的方法[html5shiv]
<!-- more -->

	<!--[if lt IE 9]>
    	<script src="bower_components/html5shiv/html5shiv.js"></script>
	<![endif]-->

[html5shiv]:https://github.com/aFarkas/html5shiv

jQuery 有 jQuery.support.html5Clone 會檢查閱覽器是否支援html5的tag，在
jQuery 1.9以前的版本有jQuery.clean 會負責處理舊版IE在插入新的tag會遇到的issue。

另外還有`display:inline`的問題，在閱覽器在解釋不支援的tag時樣式會預設為`display:inline`
所以要Reset CSS。