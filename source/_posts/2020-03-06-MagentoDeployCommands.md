---
title: Magento Deploy Commands
date: 2020-03-06 14:29:24
tags:
---

{% codeblock first_line:1 %}
bin/magento setup:upgrade
{% endcodeblock %}
{% codeblock first_line:2 %}
bin/magento setup:di:compile
{% endcodeblock %}

{% codeblock first_line:3 %}
bin/magento setup:static-content:deploy -f
{% endcodeblock %}

{% codeblock first_line:4 %}
bin/magento indexer:reindex
{% endcodeblock %}

{% codeblock first_line:5 %}
rm -rf generated/* var/cache var/di var/generation var/page_cache
rm -rf pub/static/* var/view_preprocessed
{% endcodeblock %}

{% codeblock first_line:7 %}
bin/magento deploy:mode:set production
{% endcodeblock %}