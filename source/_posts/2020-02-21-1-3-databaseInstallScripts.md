---
title: 1.3 Database Install Scripts
date: 2020-02-19 18:45:35
tags: Magento 2
categories: WEB
toc: true
---

安裝 Magento 2 Schema 
安裝 Magento 2 Data
<!-- more -->
Install Schema scripts
InstallData scripts


SchemaSetupInterface => 提供所有和資料庫相關的功能
ModuleContextInterface => 提供我們所建立的 Model 資訊


{% codeblock lang:sql first_line:1 執行以下SQL刪除掉已安裝過 Module 的紀錄 %}
delete from setup_module where module = 'Mastering_SampleModule'
{% endcodeblock %}