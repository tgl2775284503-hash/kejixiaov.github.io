---
layout: default
title: "教程目录"
---

<!-- 页面内容 -->
<header>
  <a href="https://www.youtube.com/..." target="_blank">科技小V YouTube 视频入口</a>
</header>

<h1>教程目录</h1>

<!-- 教程目录列表 -->
<ul>
  {% assign tutorials = site.pages | where: "category", "tutorial" %}
  {% for page in tutorials %}
    {% if page.url != "/" %}
      <li><a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

<!-- 广告部分内容 -->
<footer>
  <p>科技小V · 教程中心</p>
</footer>
