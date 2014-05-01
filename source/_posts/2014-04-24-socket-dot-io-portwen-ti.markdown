---
layout: post
title: "socket.io Port問題"
date: 2014-04-24 23:09:10 +0800
comments: true
categories: ["socket.io"]
---

前端連接socket.io server遇到port問題的解決方法。
<!-- more -->

### haproxy
[configure-haproxy-to-scale-multiple-nodes-with-stickiness-and-ssl]   
[using-haproxy-with-socket-io-and-ssl]    
這個方法有在Centos上面實作過是可行的，網路也有不少設定可以參考，不過當初只有測試websocket的方法。

### nginx
[nginx-websockets-ssl-and-socket-io-deployment]  
nginx在1.3之後支援websocket可以最為反向代理，這個方法沒有實測過。

### 透過改寫xhr-polling 
[how-to-make-socket-io-work-behind-nginx-mostly]    
這個方法是改寫xhr-polling的方法，前端就可以不用加上port就可以直接連接server，但是就不能使用其他的
連接方法了吧?

[how-to-make-socket-io-work-behind-nginx-mostly]: http://stephenbelanger.com/2011/09/21/how-to-make-socket-io-work-behind-nginx-mostly/

[nginx-websockets-ssl-and-socket-io-deployment]: http://blog.mixu.net/2011/08/13/nginx-websockets-ssl-and-socket-io-deployment/

[configure-haproxy-to-scale-multiple-nodes-with-stickiness-and-ssl]:http://blog.davidmisshula.com/blog/2013/02/04/configure-haproxy-to-scale-multiple-nodes-with-stickiness-and-ssl/

[using-haproxy-with-socket-io-and-ssl]: http://blog.carbonfive.com/2013/05/02/using-haproxy-with-socket-io-and-ssl/