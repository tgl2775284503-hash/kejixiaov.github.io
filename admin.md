---
layout: default
title: 教程管理后台
permalink: /admin.html
---

<div style="margin: 14px 0; padding: 12px 14px; border: 1px solid #ddd; border-radius: 10px;">
  <a href="{{ site.baseurl }}/" style="margin-right: 14px;">⬅ 返回教程目录</a>
  <a href="{{ site.baseurl }}/admin.html">🛠 返回管理后台</a>
</div>

# 🛠 教程管理后台（自动生成）

> 说明：
> - 本页面 **自动读取所有教程文件**
> - 点击「直接编辑」可跳转到 GitHub 编辑页面
> - 仅用于你自己日常维护 / 更新 / 查找

---

## 📘 教程列表（自动）

<ul>
{% assign tutorials = site.pages | where: "category", "tutorial" | sort: "date" | reverse %}
{% for page in tutorials %}
  <li>
    <strong>{{ page.title }}</strong><br>
    文件：<code>{{ page.path }}</code><br>
    <a href="https://github.com/tgl2775284503-hash/kejixiaov/edit/main/{{ page.path }}" target="_blank">
      ✏️
