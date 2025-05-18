---
title: 电信网关HG6201T获取超级账户
slug: telecom-gateway-hg6201t-get-super-account-z25sonm
url: /post/telecom-gateway-hg6201t-get-super-account-z25sonm.html
date: '2024-03-02 22:11:57+08:00'
lastmod: '2025-05-19 00:25:29+08:00'
tags:
  - 使用技巧
keywords: 使用技巧
toc: true
isCJKLanguage: true
---



# 电信网关HG6201T获取超级账户

1. 打开浏览器，打开[http://192.168.1.1:8080/cgi-bin/baseinfoSet.cgi](http://192.168.1.1:8080/cgi-bin/baseinfoSet.cgi)
2. 找到与以下类似的位置 "baseinfoSet\_TELECOMACCOUNT":"telecomadmin", "baseinfoSet\_TELECOMPASSWORD":"120&105&112&105&103&115&113&101&104&113&109&114&48&50&48&50&55&48&48&62&",\`

第一行为超级管理账户名：telecomadmin 第二行为超级管理密码：120&105&112&105&103&115&113&101&104&113&109&114&48&50&48&50&55&48&48&62&

当然，第二行的密码还需要进行一步处理.

1. 将密码进行转换，由ASCII码转为字符。
