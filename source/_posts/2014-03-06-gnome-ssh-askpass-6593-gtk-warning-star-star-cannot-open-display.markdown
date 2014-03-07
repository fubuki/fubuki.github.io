---
layout: post
title: "(gnome-ssh-askpass:6593): Gtk-WARNING **: cannot open display"
date: 2014-03-06 21:33:56 +0800
comments: true
categories: git
---

之前在使用git push 程式碼到github上面出現了上述的錯誤。看起來像是gtk跟ssh的問題，  
今天又遇到了就想辦法解決這個問題，

> ssh-askpass-gnome  
> interactive X program to prompt users for a passphrase for ssh-add  

似乎是為了使用者在GUI界面下填入ssh相關資訊的程式，只要關掉他就好了，  

> unset SSH_ASKPASS
