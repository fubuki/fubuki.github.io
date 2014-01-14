---
layout: post
title: "使用 Single User Mode 修改 Linux 密碼"
date: 2015-01-13 22:19:55 +0800
comments: true
categories: ["linux"]
---

<!-- more -->

之前在管理虛擬機的時候有些機器以前人部署的，所以完全無法得知登入密碼，後來透過網路得知 Linux 有個
 `Single User Mode` 可以讓使用者這個模式不用密碼登入主機，然後就可以透過 `passwd` 更改密碼。


 要進入 `Single User Mode` 是要在開機時在 Grub 選單在開機的指令後面加上 single 參數，然後 ctrl + x 開機
 就會進入 `Single User Mode` ，但是在我的 ubuntu 14.04 LTS 上面測試卻行不通，會顯示 `give root password for maintenance single`
 這串訊息，這時就要用另外一種方法。


 如果使用 single 參數行不通就換成 `rw init=/bin/bash`， 然後按下 ctrl + x 開機就會直接進去主機，之後使用 passwd 更改密碼即可。