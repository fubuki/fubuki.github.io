---
layout: post
title: "使用 xsendfile 提升下載性能"
date: 2014-05-07 21:21:43 +0800
comments: true
categories: ["server"]
---

X-sendfile 可以讓Server控制下載的流程，讓開發者可以透過傳送特定的header控制存取檔案的權限。
<!-- more -->

下面三種伺服器支援的header，伺服器不一定會預設支援X-sendfile，需要自己開啟相關的模組。

<table border="1">
 <tr>
  <th>     web server  </th>
  <th>     header  </th>
 </tr>
 <tr>
  <td>     apache  </td>
  <td>     X-Sendfile  </td>
 </tr>
 <tr>
  <td>     nginx  </td>
  <td>     X-Accel-Redirect  </td>
 </tr>
 <tr>
  <td>     lighttpd  </td>
  <td>     X-LIGHTTPD-send-file  </td>
 </tr>
</table>

nginx下 php的寫法。

	<?php
    $filePath = '/download/example.rar';
    header('Content-type: application/octet-stream');
    header('Content-Disposition: attachment; filename="' . basename($file) . '"');
    header('X-Accel-Redirect: '.$filePath);

nginx的 config設定。

	location /protected/ {
  		internal;
 	 	alias   /some/path/; # note the trailing slash
	}

nginx header參數

	X-Accel-Limit-Rate: 1024
	X-Accel-Buffering: yes|no
	X-Accel-Charset: utf-8