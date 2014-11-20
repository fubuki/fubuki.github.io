---
layout: post
title: "RESTful API 的版本控制"
date: 2014-10-15 23:21:36 +0800
comments: true
categories: ["API"]
---

紀錄一些如何對 RESTful API 進行版本控制的方法。

<!-- more -->


#### URI

	https://api.example.com/v1/places

#### Hostname

	https://api-v1.example.com/places

#### Body and Query Params

	1 POST /places HTTP/1.1
	2 Host: api.example.com
	3 Content-Type: application/json
	4
	5 {
	6 "version" : "1.0"
	7 }

####  Custom Request Header

[Bad HTTP API Smells: Version Headers]

[Bad HTTP API Smells: Version Headers]:http://www.mnot.net/blog/2012/07/11/header_versioning

#### Content Negotiation

[Github Media Types]

[Github Media Types]:https://developer.github.com/v3/media/#api-v3-media-type-and-the-future

#### Content Negotiation for Resources


#### Feature Flagging




#### 參考資料

1. Build APIs You Won’t Hate
2. [Your API versioning is wrong, which is why I decided to do it 3 different wrong ways ]

[Your API versioning is wrong, which is why I decided to do it 3 different wrong ways ]:http://www.troyhunt.com/2014/02/your-api-versioning-is-wrong-which-is.html