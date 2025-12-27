---
layout: default
title: 管理后台
permalink: /admin/
---

<div style="margin: 14px 0; padding: 12px 14px; border: 1px solid #ddd; border-radius: 10px;">
  <a href="{{ site.baseurl }}/" style="margin-right: 14px;">⬅ 返回教程目录</a>
  </div>

# 🛠 教程管理后台（自动生成）

---

## 📘 目录列表（自动）

<ul>
{% assign tutorials = site.pages | where: "category", "tutorial" | sort: "date" | reverse %}
{% for page in tutorials %}
  <li>
    <strong>{{ page.title }}</strong><br>
    文件：<code>{{ page.path }}</code><br>
    <a href="https://github.com/tgl2775284503-hash/kejixiaov/edit/main/{{ page.path }}" target="_blank">
      ✏️
