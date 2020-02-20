---
title: 1.1 New Module Declaration
date: 2020-02-19 18:45:35
tags: Magento 2
categories: WEB
toc: true
---

主要是新建一個 Magento Module。
透過指令
摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要
摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要
摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要摘要
<!-- more -->

---
#### Module location

> app > code 
---
#### Module registration
我們開的folder，主要是namespace and module
比如 Mastering 是 namespace 
SampleModule 是 module
---
#### Module registrationModule versioning and dependency

在Magento 2 所有的檔案
In magento 2 all files related to a module including code tests configuration and templates should be stored inside a single module directory.
第一個必要檔案就是 Module 的 registration.php 檔案
第二個需要的模組元件就是 xml 檔，將放在etc資料夾底下
{% img  https://i.imgur.com/VRZDu3S.jpg '"URN highlighter不可識別" "預設PHPStrom 不認得紅色區的文字"' %}
因為預設像 IDE PHPStrom 不認得紅色區的文字，即 {% link URNs (Uniform Resource Names) https://devdocs.magento.com/guides/v2.3/config-guide/cli/config-cli-subcommands-urn.html %}，可以透過指令去識得。

{% codeblock first_line:1 %}
bin/magento dev:urn-catalog:generate .idea/misc.xml
{% endcodeblock %}
下完指令之後，就會看到紅色的文字變綠色的。
{% img  https://i.imgur.com/UAXMnPT.jpg '"URN highlighter可識別" "指令下完後，IDE PHPStrom就能識別"' %}

{% codeblock first_line:2 %}
bin/magento module:enable Mastering_SampleModule
{% endcodeblock %}

可以在config 裡看到Mastering_SampleModule Module已經生成。
{% codeblock first_line:3 %}
bin/magento s:up
{% endcodeblock %}


可從DB 查詢
{% codeblock first_line:4 %}
select * from setup_module where module ='Mastering_SampleModule';
{% endcodeblock %}
---

#### Pestle的使用
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
