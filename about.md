---
layout: page
title: About
permalink: /about/
---

{% assign resume = site.data.resume %}

## Profile

{{ resume.profile.summary }}

## Education

{% for item in resume.education %}
<div class="list-card">
  <div class="list-card-head">
    <div>
      <h3>{{ item.school }}</h3>
      <p class="muted">{{ item.degree }}</p>
    </div>
    <span class="pill">{{ item.dates }}</span>
  </div>
  <p>{{ item.location }} · {{ item.note }}</p>
</div>
{% endfor %}

## Coursework

<div class="tag-cloud">
{% for course in resume.coursework %}
  <span class="tag">{{ course }}</span>
{% endfor %}
</div>

## Skills

{% for group in resume.skills %}
<div class="list-card">
  <h3>{{ group.category }}</h3>
  <div class="tag-cloud">
  {% for item in group.items %}
    <span class="tag">{{ item }}</span>
  {% endfor %}
  </div>
</div>
{% endfor %}

## Achievements

<ul class="compact-list">
{% for award in resume.awards %}
  <li>{{ award }}</li>
{% endfor %}
</ul>