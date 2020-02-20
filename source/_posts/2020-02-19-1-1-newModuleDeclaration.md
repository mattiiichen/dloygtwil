---
title: 1.1 New Module Declaration
date: 2020-02-19 18:45:35
tags: Magento 2
categories: WEB
toc: true
---

主要是新建一個 Magento Module。
摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要
摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要
摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要
<!-- more -->

### 主要方法
Module location
Module registration
Module versioning and dependency

在Magento 2 所有的檔案
In magento 2 all files related to a module including code tests configuration and templates should be stored inside a single module directory.
第一個必要檔案就是 Module 的 registration.php 檔案
bin/magento dev:urn-catalog:generate .dea/misc.xml
bin/magento module:enable Mastering_SampleModule
下完之後，就可以在config 裡看到 Module
bin/magento s:up

可從DB 查詢
select * from setup_module where module ='Mastering_SampleModule';

#### Pestle的使用
Pestle 中文翻譯為「杵」，像是磨藥的搗棒，延伸為是 Magento 2 程式碼生成的命令指令集。
官方主要的解譯為：
> A collection of command line scripts for Magento 2 code generation, and a PHP module system for organizing command line scripts.
##### aaa

sdfds
##### bbb
dsfdsf
###### ccc
ddsf
取得位址：
{% codeblock line_number:true first_line:1 %}
curl -LO http://pestle.pulsestorm.net/pestle.phar
{% endcodeblock %}


生成 Magento 2 Module 必要相關檔案
{% codeblock first_line:2 %}
php pestle.phar generate_module
{% endcodeblock %}


之後會有三個參數輸入，自行取名：
> 1. Namespace
> 2. Module Name
> 3. Version

除了 Pestle，Magento 2 另一個好用工具：n98-magerun2 可參考。
