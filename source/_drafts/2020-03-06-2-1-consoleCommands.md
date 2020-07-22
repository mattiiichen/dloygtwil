---
title: 2.1 Console Commands
date: 2020-03-06 17:54:38
tags:
---

Magento 2 CLI
Custom console commands implementation



Magento 2 command line interface
custom console commands implementation

先建立一個console command 主要能夠新增 items 到我們的items table 裡。

先在 Module 裡建 Console/Command/Additem.php

Magento 2 有使用symphony component console
所以要importing 一些 symphony的元件