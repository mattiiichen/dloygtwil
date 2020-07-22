---
title: Magento Deploy Commands
date: 2020-03-06 14:29:24
tags:
---

{% codeblock first_line:1 %}
rm -rf generated/* var/cache var/di var/generation var/page_cache
rm -rf pub/static/* var/view_preprocessed
{% endcodeblock %}

{% codeblock first_line:2 %}
bin/magento setup:upgrade
{% endcodeblock %}
{% codeblock first_line:3 %}
bin/magento setup:di:compile
{% endcodeblock %}

{% codeblock first_line:4 %}
bin/magento setup:static-content:deploy -f
{% endcodeblock %}

{% codeblock Acer Local 靜態佈版，digitalstore1 基本會佈 %}
bin/magento s:s:d -f --exclude-theme Alothemes/digitalstore1 --exclude-theme Alothemes/digitalstore2 --exclude-theme Alothemes/digitalstore3 --exclude-theme Alothemes/digitalstore4 --exclude-theme Alothemes/digitalstore5
{% endcodeblock %}


{% codeblock first_line:5 %}
bin/magento indexer:reindex
{% endcodeblock %}



{% codeblock first_line:6 %}
bin/magento deploy:mode:set production
{% endcodeblock %}