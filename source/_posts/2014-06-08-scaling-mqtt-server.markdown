---
layout: post
title: "Scaling mqtt server"
date: 2014-06-08 23:59:01 +0800
comments: true
categories: ["mqtt"]
---

目前測試過幾套mqtt broker，記錄一下使用過的心得和擴展方案。
<!-- more -->

目前用過以下幾種broker:  
1. [mosca]  
2. [rabbitmq]  
3. [mosquitto]  


[mosca]:https://github.com/mcollina/mosca
[rabbitmq]:http://www.rabbitmq.com/
[mosquitto]:http://mosquitto.org/

## mosca
使用node.js寫成的broker，負責pubsub和持久化的部分可以由使用者自行自訂，程式碼也不會太過於龐大，原本
要使用這個當mqtt server在擴展上可以透過共用pubsub和持久化的部分擴展，不過在處理offline message上有問題就放棄了。


## rabbitmq
使用erlang寫成的broker，rabbitmq透過plugin的方式支援mqtt協定，支援到mqtt 3.1，rabbitmq原本就支援
cluster的架構，並且session可以互相共享，讓rabbitmq在懭展的同時也能處理offline message的問題。


## mosquitto 
使用C語言寫成的，原本是利用mosquitto的bridge架構擴展server，不過在測試offline message的時候沒有辦法
處理session的問題，server之間沒有共享session，但是如果能夠自行處理offline message的問題 mosquitto 
也是個不錯的選擇。




