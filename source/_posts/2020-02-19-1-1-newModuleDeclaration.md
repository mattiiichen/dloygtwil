---
title: 1.1 New Module Declaration
date: 2020-02-19 18:45:35
tags: Magento 2
categories: WEB
toc: true
---
test
<!-- more -->


# 等級一標題
## 等級二標題
### 等級三標題
#### 等級四標題
##### 等級五標題
###### 等級六標題

Module location
Module registration
Module versioning and dependency

Magento 2 另一個好用工具：n98-magerun2
Pestle 中文翻譯為「杵」，像是磨藥的搗棒，延伸為是 Magento 2 程式碼生成的命令指令集。
官方主要的解譯為：
> A collection of command line scripts for Magento 2 code generation, and a PHP module system for organizing command line scripts.
取得位址：
> curl -LO http://pestle.pulsestorm.net/pestle.phar

生成 Magento 2 Module 必要相關檔案
php pestle.phar generate_module
之後會有三個參數輸入：
> 1. Namespace
> 2. Module Name
> 3. Version

> bin/magento s:up