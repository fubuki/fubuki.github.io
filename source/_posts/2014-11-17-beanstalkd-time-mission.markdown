---
layout: post
title: "使用 beanstalkd 設定特定時間執行任務"
date: 2014-11-17 22:30:27 +0800
comments: true
categories: ["queue"]
---

<!-- more -->


最近工作上需要設定在特定時間執行設定好的任務，原本是使用 Linux 的 crontab 定時檢查是否需要執行這個任務，
然後將任務丟給 beanstalkd 執行，後來查詢 beanstalkd 和 celery 都有個 delay 的指令可以讓任務設定過多少時間後才執行。

[phalcon beanstalkd] 裡面有寫在 put 的時候加上額外的參數 `array('priority' => 250, 'delay' => 10, 'ttr' => 3600)`。  
[Can I schedule tasks to execute at a specific time?] 裡面有介紹 celey 如何指定時間處理。

此外另外有一個想法是使用 Redis 的 `Keyspace Notifications`  設定一個鍵值跟過期時間然後使用一個進程監視過期的通知然後就可以設定在
特定時間執行任務。


[Can I schedule tasks to execute at a specific time?]:http://celery.readthedocs.org/en/latest/faq.html#module-celery.task.base
[phalcon beanstalkd]:http://docs.phalconphp.com/en/latest/reference/queue.html