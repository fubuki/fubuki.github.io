---
layout: post
title: "Openresty Server"
date: 2014-12-21 22:59:33 +0800
comments: true
categories: ["nginx"]
---

<!-- more -->


[openresty] 為核心是 nginx 在外加一些第三方模組的版本。


之前在研究 nginx 跟 Lua 結合的資訊時看到了一篇 [ngx_openresty: an Nginx ecosystem glued by Lua]，
裡面介紹了 [ngx-openresty] ，並且介紹了這個基於 nginx 擴展版本裡面有哪些功能，並且從文章標題就可以
得知裡面使用 Lua 整合整個生態系統。


[openresty] 從官網看到可以透過編寫 Lua 腳本跟 mysql,redis 連線做出反向代理的功能，另外也有看到有人
使用 Lua 編寫影音加密的 Http LiveStream 的功能，看起來可以考慮將一些應用層的東西轉移到 ngix 上面藉此提高
網站的效率。



[openresty]:http://openresty.org/
[ngx-openresty]:https://github.com/openresty/ngx_openresty
[ngx_openresty: an Nginx ecosystem glued by Lua]:http://agentzh.org/misc/slides/ngx-openresty-ecosystem/#1