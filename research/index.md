---
title: Research & Publications
---

本页面展示 YS Laboratory 的科研成果，包括学术论文、科研项目与技术成果。

{% include section.html %}

## 代表性成果（Featured Publications）

{% include list.html data="citations" component="citation" filters="featured: true" %}

{% include section.html %}

## 全部成果（All Publications）

{% include list.html data="citations" component="citation" style="rich" %}

{% include section.html %}

## 按年份浏览

{% assign years = site.data.citations | map: "date" | map: "split: '-'" | map: "first" | uniq | sort | reverse %}

{% for year in years %}
### {{ year }}
{% include list.html data="citations" component="citation" filters="date: ^{{ year }}" %}
{% endfor %}
{% include section.html %}

## 期刊论文（Journal）
{% include list.html data="citations" component="citation" filters="type: journal" %}

{% include section.html %}

## 会议论文（Conference）
{% include list.html data="citations" component="citation" filters="type: conference" %}

{% include section.html %}

## 专利（Patent）
{% include list.html data="citations" component="citation" filters="type: patent" %}
