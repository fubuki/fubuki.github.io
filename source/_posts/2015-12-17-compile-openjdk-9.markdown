---
layout: post
title: "compile openjdk 9 on ubuntu"
date: 2015-12-17 22:41:33 +0800
comments: true
categories: ["java"]
---


<!-- more -->

	hg clone http://hg.openjdk.java.net/jdk9/jdk9
	cd jdk9
	bash ./get_source.sh

	install dependency package
	
	apt-get install openjdk-8-jdk
	
	bash ./configure 
	make all
	make install
