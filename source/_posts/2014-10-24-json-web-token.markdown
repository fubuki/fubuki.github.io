---
layout: post
title: "JSON Web Token"
date: 2014-10-24 21:48:13 +0800
comments: true
categories: ["javascript"]
---


<!-- more -->

最近在研究 socket.io 時看到了一個東西； [jwt] ， 後來在 mosca 也看到了相同的東西，尋找之後發現全名為 `JSON Web Token`，
是用在加密 API 的回傳值，[Using JSON Web Tokens with Node.js] 這篇文章裡面有寫說 jwt 是怎麼加密，然後在 [ietf] 有更詳細的規格，
另外在 [Authenticating & Authorizing Devices using MQTT with Auth0] 有寫如何跟 mosca server 一起使用，目前看起來是可以期待未來用在工作上面
，github 上面已經有些範例和函式庫可以使用，也許可以用在目前有使用 mqtt 的應用程式上面提高安全性。


[jwt]:http://jwt.io/]
[Using JSON Web Tokens with Node.js]:http://www.sitepoint.com/using-json-web-tokens-node-js/
[Authenticating & Authorizing Devices using MQTT with Auth0]:https://docs.auth0.com/scenarios-mqtt
[ietf]:http://tools.ietf.org/html/draft-ietf-oauth-json-web-token-19