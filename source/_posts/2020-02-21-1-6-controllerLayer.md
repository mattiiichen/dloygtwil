---
title: 1.6 Controller Layer
date: 2020-02-21 16:48:37
tags: Magento 2
categories: WEB
toc: true
---


Routing
Fronted controllers
Backend controllers
<!-- more -->
Layer implementation is a routing configuration
Layer的實作即是 Routing 的設置
Magento 2 有兩個路由：一個 Fronted area 和一個是 Backend area
Controller 建立之後要先建立路由



{% codeblock first_line:1 當每次更改 XML 檔時，一定要跑的指令，因為 XML 檔案會被 Magento 2 Cache 住。 %}
bin/magento c:f
{% endcodeblock %}

可以把 Admin 的 URL 上的 Key 關掉
STORES > Configuration > Advanced > Admin > Security > Add Secret Key to URLs > Use system value > No > Save Config