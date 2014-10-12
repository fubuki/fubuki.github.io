---
layout: post
title: "PHP with composer"
date: 2014-09-10 22:52:45 +0800
comments: true
categories: ["php"]
---

<!-- more -->

以前在安裝 PHP 的插件通常是透過 PEAR 安裝的，然後每個插件就要手動一個個安裝，不過現在有 [composer] 這個相依性管理工具，
用起來跟 NPM 感覺差不多，只要定義好需要用哪些套件和版本就會幫忙安裝好。

###安裝方法
	curl -sS https://getcomposer.org/installer | php  
	mv composer.phar /usr/local/bin/composer 


###基本用法



[composer]:https://getcomposer.org/