---
layout: post
title: "git-reflog的用法"
date: 2014-04-07 21:11:57 +0800
comments: true
categories: ['git']
---

之前看到一篇去年的消息Jenkins開發者意外的抹消掉在github上一個月的commit，這跟Github的設定和
使用者本身使用強制推送有關，如果想要知道詳細情形請參照['這裡']。
<!-- more -->

不過裡面比較引我注意的是他如何回復被蓋掉的部分，利用git-reflog可以取得被刪除的commit，之後再開出
一個新的分支取回原本的版本，這個跟git-log 的差異在git-log只會顯示過去提交過的記錄，但是reflog會顯示
所有的變更紀錄，下面幾個我比較常用的指令都會紀錄在reflog裡面，藉此如果版本有問題了話更容易回復。

* branch
* commit
* checkout
* pull
* push
* merge
* clone
* branch
* stash


git-reflog OPTIONS
==================
*  --stale-fix

*  --expire=<time>

*  --expire-unreachable=<time>

*  --all

*  --updateref

*  --rewrite

*  --verbose

['這裡']: https://groups.google.com/forum/#!msg/jenkinsci-dev/-myjRIPcVwU/t4nkXONp8qgJ