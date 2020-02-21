---
title: 1.4 Database Upgrade Scripts
date: 2020-02-21 15:57:40
tags: Magento 2
categories: WEB
toc: true
---


最大的差異就是 Version Number 要清楚，Upgrade Scripts 會先判斷 Module version 是不是大於小於，才會做升級步驟。

<!-- more -->

{% codeblock first_line:1 執行 Magento 升級指令 %}
bin/magento s:up
{% endcodeblock %}


{% codeblock lang:sql first_line:1 查詢是否有更新資料 %}
select * from mastering_sample_item;
{% endcodeblock %}