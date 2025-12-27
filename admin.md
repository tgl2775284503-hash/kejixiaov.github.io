---
layout: default
title: 教程管理后台（仅作者使用）
---

# 🛠 教程管理后台（自动生成）

> 说明：  
> - 本页面 **自动读取所有教程文件**  
> - 点击「编辑」可直接跳转到 GitHub 编辑页面  
> - 本页主要用于 **日常维护 / 更新 / 查找**

---

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
