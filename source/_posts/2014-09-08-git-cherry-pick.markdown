---
layout: post
title: "git cherry-pick"
date: 2014-09-08 22:46:39 +0800
comments: true
categories: ["git"]
---

<!-- more -->


在看 `Android 核心剖析` 時得知一個有趣的命令 `git cherry-pick` ，似乎是可以取得單獨的 commit 然後
合併到目前的分支，如果專案在多分支開發的時候，有些需要在多個分支加入同一份修改的時候可以使用 `git cherry-pick`，
避免分支合併到不需要的 commit。