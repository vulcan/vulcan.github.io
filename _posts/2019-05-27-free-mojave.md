---
layout: post
title:  "解决Mojave在内网卡顿的问题"
date:   2019-05-27 22:02:02
categories: Misc
---
去年9月份升级Mac OS Mojave版本，几乎把办公电脑给废掉了，在公司内网使用时很多应用启动时需要几分钟，非常卡顿，遍寻方案无解。奇怪的是关闭WiFi，或者连接家中的WiFi这个症状就消失了。

今天终于在内网找到了解决的办法，在hosts文件中，增加`127.0.0.1 ocsp.apple.com`, 问题解决了！
查了了这个服务器的问题，是苹果的证书服务器，应该是很多应用在启动时会去该服务器验证证书，而在内网中屏蔽了某些网址，造成了应用启动慢了。

终于可以正常使用Mac了，Free Coding！