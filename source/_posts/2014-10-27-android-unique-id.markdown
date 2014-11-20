---
layout: post
title: "android unique id"
date: 2014-10-27 22:59:45 +0800
comments: true
categories: ["android"]
---

如何取得 android 裝置的唯一編號。

<!-- more -->

目前有一些用來識別是否為同一個裝置的方法，不過都有各自的問題。

1. Mac Address
在沒有 wifi 或是沒有開啟 wifi 的裝置就無法取得 Mac Address。

2. DeviceId(IMEI/MEID/ESN)
非手機裝置會沒有 DeviceId，另外似乎有些產品會返回 null。

3. Android ID
有些廠商的裝置會有相同的 Android ID，但是是哪些廠商我就沒有看過有人寫出來。 

4. Serial Number
在 2.3之後的版本可以透過 android.os.Build.SERIAL 取得 Serial Number，似乎需要 READ_PHONE_STATE的權限，

5. UUID
開發者可以在 APP 安裝時產生 UUID，但是就必須考慮到如何保存 UUID 的數值。



參考:  
[Identifying App Installations]  
[Android Unique Device ID]  

[Identifying App Installations]:http://android-developers.blogspot.tw/2011/03/identifying-app-installations.html
[Android Unique Device ID]:http://www.pocketmagic.net/2011/02/android-unique-device-id/