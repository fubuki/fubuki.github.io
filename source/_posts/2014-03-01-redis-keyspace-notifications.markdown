---
layout: post
title: "Redis Keyspace Notifications"
date: 2014-03-01 09:09:10 +0800
comments: true
categories: redis
---
http://redis.io/topics/notifications  
redis 在2.8版本新增的功能，鍵值可以發出事件通知，可以利用PUBSUB的功能
接受到相關的通知。

<!-- more -->
K     Keyspace events, published with __keyspace@<db>__ prefix.  
E     Keyevent events, published with __keyevent@<db>__ prefix.  
g     Generic commands (non-type specific) like DEL, EXPIRE, RENAME, ...  
$     String commands  
l     List commands  
s     Set commands  
h     Hash commands  
z     Sorted set commands  
x     Expired events (events generated every time a key expires)  
e     Evicted events (events generated when a key is evicted for maxmemory)  
A     Alias for g$lshzxe, so that the "AKE" string means all the events.  