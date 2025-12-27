---
layout: default
title: "教程目录"
---

<!-- 页面内容 -->
<h1>教程目录</h1>

<!-- 教程目录列表 -->
<ul>
    {% assign tutorials = site.pages | where: "category", "tutorial" %}
    {% for page in tutorials %}
        {% if page.url != "/" %}
            <!-- 使用 relative_url 确保生成正确的链接 -->
            <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
        {% endif %}
    {% endfor %}
</ul>

<!-- 广告部分内容 -->
<footer>
</footer>
