---
title: Home
layout: default
nav_order: 1
---

# 환영합니다! 👋

**직관적 개발자**에 오신 것을 환영합니다! 이 블로그는 **컴퓨터 과학**과 **프로그래밍**의 기본 원리부터 고급 개념까지, **개발자가 직관적으로 이해하고 성장할 수 있는 지식**을 공유하는 공간입니다.

## 최근 수정된 페이지 목록

<ul>
  {% assign filtered_pages = site.pages | where: "layout", "page" %}
  {% assign sorted_pages = filtered_pages | sort: "last_modified_at" %}
  {% assign recent_pages = sorted_pages | reverse %}
  {% for page in recent_pages limit:10 %}
    <li>
      <a href="{{ page.url | absolute_url }}">{{ page.title }}</a>
      <p>{{ page.excerpt | strip_html | truncatewords: 20 }}</p>
      <small>수정일: {{ page.last_modified_at | date: "%Y년 %m월 %d일" }}</small>
    </li>
  {% endfor %}
</ul>