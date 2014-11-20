---
layout: post
title: "Gearman 和 Beanstalk"
date: 2014-06-05 23:41:22 +0800
comments: true
categories: ["queue"]
---

記錄一下之後要研究和測試這兩種消息隊列。
<!-- more -->

目前在工作上是用[beanstalkd]作為消息隊列，由於使用人數少所以也不會有什麼問題，不過在PHP conf上面看到有人提了一個[gearman]的消息隊列，
這兩個消息隊列都是用C語言撰寫的，在client library方面都有支援PHP和Node.js，不過似乎[gearman]的使用人數比較多的樣子，之後先研究這兩者
的管理工具[beanstalk_console]和[gearmanui]和擃展性。




[gearman]: http://gearman.org/
[beanstalkd]: https://github.com/kr/beanstalkd
[gearmanui]:https://github.com/gaspaio/gearmanui
[beanstalk_console]:https://github.com/ptrofimov/beanstalk_console