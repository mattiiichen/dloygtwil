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
Controller建立前，要先有路由。

app/code/Mastering/SampleModule/etc/adminhtml/routes.xml
app/code/Mastering/SampleModule/etc/frontend/routes.xml


Controller Layer implementation is a routing configuration
Controller Layer的實作即是 Routing 的設置
Magento 2 有兩個路由：一個 Fronted area 和一個是 Backend area
Controller 建立之後要先建立路由
記得Backend area 是Adminhtml folder


{% codeblock first_line:1 當每次更改 XML 檔時，一定要跑的指令，因為 XML 檔案會被 Magento 2 Cache 住。 %}
bin/magento c:f
{% endcodeblock %}

{% codeblock first_line:2 Admin 的 URL 上的 Key 關掉 %}
STORES > Configuration > Advanced > Admin > Security > Add Secret Key to URLs > Use system value > No > Save Config
{% endcodeblock %}
經過驗証，Controller更改的時候，需要cache:flush才會生效，在某些部份情況下會這樣。
而資料庫直接異動的話，也是要cache flush ，browser再重load 才會生效。

Mastering/SampleModule/Controller/Adminhtml/Index/Index.php
    class Index extends \Magento\Backend\App\Action
Mastering/SampleModule/Controller/Index/Index.php
    class Index extends \Magento\Framework\App\Action\Action