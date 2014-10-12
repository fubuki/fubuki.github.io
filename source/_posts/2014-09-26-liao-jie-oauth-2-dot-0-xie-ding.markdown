---
layout: post
title: "了解 OAuth 2.0  協定"
date: 2014-09-26 23:39:06 +0800
comments: true
categories: ["oauth"]
---

最近需要建立 OAuth 2.0 的服務便去尋找一些相關的資訊。

<!-- more -->


[The OAuth 2.0 Authorization Framework] 描述關於整個 OAuth 2.0 的 SPEC，有人已經轉換成 [markdown 的版本]看完後
便大致了解了目前在網路那些 OAuth 2.0 的 Library 並且去使用它們。


目前工作上是使用 [oauth2-server] 這個專案，使用的是 `Password` 的 grant type，透過輸入帳密取得 token 。


#### Grant type

1. Authorization Code
2. Implicit
3. Resource Owner Password Credentials
4. Client Credentials





[The OAuth 2.0 Authorization Framework]:http://tools.ietf.org/html/rfc6749
[markdown 的版本]:https://gist.github.com/chitsaou/6590756
[oauth2-server]:https://github.com/thephpleague/oauth2-server