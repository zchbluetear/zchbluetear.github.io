---
layout: post
title: "副路由器开启WDS功能连接主路由器上网"
pid: 2014081501
comments: true
keywords: "WDS"
description: ""
categories: [学习笔记]
tags: [Router, WDS]
---
**背景:** 新买了一台台式电脑, 没有无线网卡, 而且由于场地原因, 无法直接使用网线将电脑和路由器连接起来, 致使台式机无法上网.

**解决思路:** 再使用一台路由器, 开启路由器的WDS功能, 连接主路由器. 台式电脑使用网线连接副路由器后上网.

**目标:** 主路由器使用ADSL拨号, 副路由器开启WDS连接主路由器. 电脑连接到副路由器后可以正常上网.

**设置:**

1. 使主路由器能够正常上网.
2. 连接到副路由器后设置副路由器的无线设置, 选择开启WDS功能, 并扫描SSID列表, 选择主路由器的SSID, 选择正确的信道和加密方式, 输入密码, 保存.
3. 关闭副路由器的DHCP功能(默认主路由器开启了DHCP功能).
4. 设置副路由器的WAN口IP与主路由器LAN口IP在一个网段内. 假设主路由器的LAN口IP为`192.168.0.1`, 则设置副路由器的WAN口IP为`192.168.0.2`.
5. 设置副路由器的WAN口IP后, 副路由器会自动重启. 重启后正常情况下连接到副路由器的电脑就可以正常上网了.