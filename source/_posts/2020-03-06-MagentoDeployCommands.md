---
title: Magento Deploy Commands
date: 2020-03-06 14:29:24
tags:
---

{% codeblock first_line:1 %}
rm -rf generated/* var/cache var/di var/generation var/page_cache
rm -rf pub/static/* var/view_preprocessed
{% endcodeblock %}