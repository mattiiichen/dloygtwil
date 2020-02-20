---
title: 1.1 New Module Declaration
date: 2020-02-19 18:45:35
tags: Magento 2
categories: WEB
toc: true
---
主要是新建一個 Magento Module。

<!-- more -->
Module location
Module registration
Module versioning and dependency



### Pestle的使用
Pestle 中文翻譯為「杵」，像是磨藥的搗棒，延伸為是 Magento 2 程式碼生成的命令指令集。
官方主要的解譯為：
> A collection of command line scripts for Magento 2 code generation, and a PHP module system for organizing command line scripts.

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
