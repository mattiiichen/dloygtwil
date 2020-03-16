---
title: 4 Customization
date: 2020-03-06 17:43:16
tags: Master and Test Magento 2 with Ease
---


#### 4.1 Dependecy injection configuration
依賴注入
Preferences
Arguments
Virtual types
<!-- more -->
用 Login functionality 做範例

主要先進入
Mastering/SampleModule/Console/Command
只要call 這個command 就會新增item
bin/magento mastering:item:add thesummary

Dependence injection configuration 檔案會在 每個 Module 裡的 etc 下的 di.xml

和另一個全域的 
app/etc/di.xml
基本的 Logger 功能，都會在這支上面。
看看這一支檔案第一行，就是在定義一個 logger interface

若使用 \<preference\> 的方式，會作用到「所有功能」，所以就用 type arguments 
{% codeblock lang:xml line_number:true first_line:1 %}
<virtualType name="MasteringLogger" type="Magento\Framework\Logger\Monolog">
    <arguments>
        <argument name="name" xsi:type="string">main</argument>
        <argument name="handlers"  xsi:type="array">
                <item name="system" xsi:type="object">Magento\Framework\Logger\Handler\System</item>
                <item name="debug" xsi:type="object">Mastering\SampleModule\Model\DebugHandler</item>
        </argument>
    </arguments>
</virtualType>
{% endcodeblock %}

虛擬 Type 會 base 在基本的 Magento\Framework\Logger\Monolog
而不一樣的是 Argument


#### 4.2 Plugins and observers
#### 4.3 Layout configuration
#### 4.4 JavaScript customization



若是在Prodction Mode就要清處 pub/static folder然後重新佈暑這些靜態內容
若在 Develop Mode 可以留下，但也是可以清掉

{% codeblock lang:objc line_number:true first_line:1 %}
var config = {
    'map': {
        '*': {
            'mage/validation': 'Mastering_SampleModule/js/validation'
        }
    },
    config: {
        mixins: {
            'Mastering_SampleModule/js/validation': {
                'Mastering_SampleModule/js/validation-mixin': true
            }
        }
    }
};
{% endcodeblock %}
{% codeblock line_number:true first_line:1 %}
mage/validation => lib/web/mage/validation.js
Mastering_SampleModule/js/validation => app/code/Mastering/SampleModule/view/frontend/web/js/validation.js
{% endcodeblock %}


pub/static/_requirejs/        ==> 給Requirejs使用
pub/static/frontend/
pub/static/deployed_version.txt

也包含
var/cache/
var/page_cache/
var/view_preprocessed/



It was empty email field will show us this is required to Custom message.
It means that our file from our module is served in default validation file.

最後面，我覺得是刻意把所有的validation 設定成 True ，導致所有的驗証成為「已驗証 (Validated)」，把這樣的結果 mixin 到 module validation.js (是混合還是append 上去？)。
最後驗証結果，就會Email 欄位留空但能 Submit 出去(因為「已驗証」) 。