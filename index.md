---
layout: default
title: 教程目录
---

# 📘 教程目录（自动更新）

<ul>
{% assign tutorials = site.pages | where: "category", "tutorial" %}
{% for page in tutorials %}
  {% if page.title and page.url != "/" %}
    <li><a href="{{ page.url }}">{{ page.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>
