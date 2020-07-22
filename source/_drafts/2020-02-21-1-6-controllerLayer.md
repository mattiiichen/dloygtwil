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


{% codeblock first_line:1 所有 Magento XML file 都會被 Cache 到 Magento 2 裡，所以當有更動任何 XML files，都需要 flush cache %}
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
    
    route front Name 即是前台在 Url 後接的名字，直接後方接/mastering 
    mastering 即是 route name 可以直接導過去。   
    app/code/Mastering/SampleModule/etc/frontend/routes.xml
    
    同樣的後台也是接在 admin/mastering 後面，就會透過 route 導到過去