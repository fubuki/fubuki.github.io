---
layout: post
title: "Yeoman Tool"
date: 2014-04-22 23:37:09 +0800
comments: true
categories: 
---

[Yeoman] 是一個開發工具，讓使用者能夠建立自己的專案環境，之前在使用Phalcon的時候都需要重新建立開發環境，
之前有看到利用Yeoman建立Angularjs的專案現在就在網路上看到[generator-phalcon]建立專案。
<!-- more -->
### Yemoan 內容
1. yo
2. Grunt
3. Bower

###安裝Yeoman  
		npm install -g yo

###建立angular的專案
		npm install -g generator-angular  
		yo angular                         
		bower install angular-ui           
		grunt test                         
		grunt server                       
		grunt                              

###安裝Phalcon 模板
		npm install generator-phalcon

[generator-phalcon]: https://www.npmjs.org/package/generator-phalcon
[Yeoman]: http://yeoman.io/