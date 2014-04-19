---
layout: post
title: "jquery bind, live, delegate, on"
date: 2014-04-14 21:28:39 +0800
comments: true
categories: ['jquery']
---

jquery 用來綁定事件的方法有好幾種根據Jquery版本不同能支援的方法也有所不同，這篇文章就短暫
記錄一下那些函式的用法，如果要更詳細的解說推薦[jQuery演進短論（TonyQ）]這個影片，講解的還蠻清楚的。
<!-- more -->

###bind
以前我使用最多的綁定方式，除了可以綁定jquery原有的函式也可以自訂事件名稱，在去觸發自訂事件，不過bind只能綁定一次如果使用者
之後append一個新的節點就必須在重新綁定一次。  

	$(body).bind("click",function(){
		console.log('click event');
	});
###live
有時候會使用ajax動態在入新的內容，開發者希望能夠自動將事件綁定到新的內容裡面就會使用live的方式去綁定，不過由於live的實現方式
如果在程式碼裡使用太多live反而會讓降低javascript的效率。
	$("#example").live("click",function(){
		console.log('click event');
	});
	$(body).append('<div id = "example"> click here</div>');

###delegate
由於live 是透過監聽document的節點達成事件動態綁定，所以並不建議使用live而是使用delegate取代，使用方法如下，綁定的事件只會在#example下的
li元素才會生效。

	$("#example").delegate("li", "click", function () {  
		console.log('click event');
	});  

###on
on是目前官方推薦使用的綁定方式，不論是bind和live都可以透過on去實現，如果有去看jquery的原始碼在某個版本之後bind和live以及delegate底層都是
用on去實現了並且在1.10的時候live就被拿掉了，如果之後有空還需要整理一下on的實現方法。  
以下同等於bind的用法

	$("#example").on("click",function(){
		console.log('click event');
	});

以下同等於live的用法

	$(document).on("click","#example",function(){
		console.log('click event');
	});


 


[jQuery演進短論（TonyQ）]: http://www.youtube.com/watch?v=znroW8mH07o