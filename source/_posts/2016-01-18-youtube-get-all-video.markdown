---
layout: post
title: "youtube get all video data"
date: 2016-01-18 21:28:46 +0800
comments: true
categories: [""]
---


<!-- more -->

1. 先從 `https://www.googleapis.com/youtube/v3/channels` 取得 `uploaded playlist id`。
2. 在使用 `https://www.googleapis.com/youtube/v3/playlistItems` 取得 `video data` 。
3. 原本想從 `search api` 取得 `vidoe data` 但是最多只能有 500 筆結果。
4. 一次 api 呼叫只能有 `50` 筆資料，超過 `50` 筆需要使用 `nextPageToken` 取得之後的資料。