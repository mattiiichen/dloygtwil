---
title: 1 Introduction
date: 2020-03-13 15:36:10
tags: Magento 2 Theme Development
---

#### 1.1 Theme Files

Next we are going to be tackling theme creation for Magento 2 what you're about to see is suitable for creating a new theme as well as a customize in an existing one.
The magento teams strongly recommend this type of practice so the changes don't compromise or even deal it is due to an update of the original theme.
So everything we're goint to learn from now on our good practices what we have here is an access to the magento control panel.
We are always going to have all the documentation within reach so you can see is quite think.
But you don't have to worry because it's going to make it easy for you so you won't have to struggle with it or spend hours looking things up in forums and going to guide you every step of the way.
More resources.
We have magento with the lumas theme which is going to be our starting point right now there are two projects that luma, Blank.
Blank contains the minimum attempt the theme has to have a luma takes it a step further. Luma is going to be foundation of our own theme because this way we're going to save us a tone of work.

也有 Frontend Developer Guide 可以參考
更多的資源 Luma theme是我們開始的起點
blank 是最小的theme 的主
luma 是theme的最基礎的架構

你可以在 https://github.com/magento/magento2 找到兩個theme，一個luma 一個blank
他們在app/design/frontend/Magento
這邊都是luma 和 blank 原始code，若有需要可以在這邊取得。 
以及還有這邊的作練習的theme的repo
https://github.com/bypixelpro/magento2temacurso
接下來著手準備Magento 2 Theme 的建立

同樣的DB裡
Select * from theme
也可以看到已安裝的theme的清單。
一個theme 最少的必要檔案有兩個：
一個是registration theme
一個是theme.xml
這兩個檔案一有，只要flush DB，theme就會在後台 Content > Theme 的清單顯示出來，真神奇。



#### 1.2 URL Images
#### 1.3 URL Static Files
#### 1.4 URL Cover
#### 1.5 Uninstall Theme