---
title: 3.1 UI Component Overview
date: 2020-03-06 15:13:20
tags:
---

ui Component layout elemnet
Magento_UI module
Ui components declaration


#### UI Component Overview
uiComponent layout element

當後台的 Page 在 loading 時，其實是 magento 2 使用 knockout.js 讓每個 UI 元件可以顯示。
可以看看 Product 的頁面和 Widgets 的頁面，新舊之分，會有點差異。
vendor\magento\module-ui\view\base\ui_component\etc\definition.xml
什麼是 massaction？

Magento_UI module
UI components declaration

Controller\Adminhtml\index\index.php

#### Admin panel grids
#### Admin panel forms
#### Checkout


當你用後台進入product list 頁面時，會看到loader 轉圈圈，是因為這個頁面所有的示素都是用knockout.js顯示出來。而這個頁面的所有元素就是 UI 元件

/Users/mattchen/Projects/magento2/vendor/magento/module-ui/view/base/ui_component/etc/definition.xml
/Users/mattchen/Projects/magento2/vendor/magento/framework/View/Layout/Element.php

Rendering Grids

Grid collection
Listing UI Component configuration
每個 UI Component 需要額外一個 Collection


16. Extending UI Components
bin/magento cache:flush
再執行 bin/magento setup:upgrade
setup:upgrade 好像已經有Cache cleared successfully
和cache:flush 有甚麼差別嗎？