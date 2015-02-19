---
layout: post
title: "nginx 的 worker_cpu_affinity 參數"
date: 2015-01-25 21:13:34 +0800
comments: true
categories: ["nginx"]
---

<!-- more -->

nginx 可以藉由使用 `worker_cpu_affinity` 在多核分配進程在哪幾顆 CPU 下執行。


四核四個進程

	worker_processes 4;
	worker_cpu_affinity 1000 0100 0010 0001;

四核兩個進程

	worker_processes 2;
	worker_cpu_affinity 1000 0001;