---
layout: default
title: 管理后台
permalink: /admin/
---

<h1 style="text-align:center;">🛠 教程管理后台（自动生成）</h1>

## 📘 教程列表（自动）

<ul>
{% assign tutorials = site.pages | where: "category", "tutorial" | sort: "date" | reverse %}
{% for page in tutorials %}
  <li>
    <strong>{{ page.title }}</strong><br>
    文件：<code>{{ page.path }}</code><br>
    <a href="https://github.com/tgl2775284503-hash/kejixiaov/edit/main/{{ page.path }}" target="_blank">
      ✏️ 直接编辑此教程
    </a>
  </li>
  <br>
{% endfor %}
</ul>

