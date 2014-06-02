---
layout: post
title: "MQTT bridge"
date: 2014-05-30 20:57:07 +0800
comments: true
categories: ["mqtt"]
---

關於mqtt bridge的功能。

<!-- more -->


日前在研究各種 `MQTT Broker` 的方案，市面上有許多方案可以使用，原本是使用[mosca]作為server但是在處理離線訊息和擴展性上
有些問題，此外讓手機端連接 [mosca] 作測試會出現 connection reset的問題，因此換用 [Mosquitto]作為替代方案，使用上沒出現
什麼問題，在擴展性上有[bridge_protocol]這個方案，可以讓一台broker作為bridge讓其他broker透過bridge互相溝通，也支援離線訊息
的功能，詳細設定可以參考[mosquitto-conf]的bridge部分。



[mosca]: https://github.com/mcollina/mosca
[Mosquitto]: http://mosquitto.org/
[bridge_protocol]: http://mqtt.org/wiki/doku.php/bridge_protocol
[mosquitto-conf]: http://mosquitto.org/man/mosquitto-conf-5.html
