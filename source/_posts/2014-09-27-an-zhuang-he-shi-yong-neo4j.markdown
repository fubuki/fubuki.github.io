---
layout: post
title: "安裝和使用 Neo4j"
date: 2014-09-27 23:45:25 +0800
comments: true
categories: ["Graph database"]
---

如何安裝和使用 Neo4j

<!-- more -->


#### 安裝

	wget -O - http://debian.neo4j.org/neotechnology.gpg.key| apt-key add - # Import our signing key
	echo 'deb http://debian.neo4j.org/repo stable/' > /etc/apt/sources.list.d/neo4j.list # Create an Apt sources.list file
	aptitude update -y # Find out about the files in our repository
	aptitude install neo4j -y # Install Neo4j, community edition


#### 使用

開啟 http://server-ip:7474，可以看到一個 web admin 然後就可以開始玩 Neo4j