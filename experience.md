---
layout: page
title: Experience
permalink: /experience/
---

{% assign resume = site.data.resume %}

{% for item in resume.experience %}
<article class="timeline-item">
  <div class="timeline-meta">
    <span class="pill">{{ item.dates }}</span>
    <span class="muted">{{ item.location }}</span>
  </div>
  <h2>{{ item.title }}</h2>
  <p class="muted">{{ item.org }}</p>
  <ul class="compact-list">
  {% for bullet in item.bullets %}
    <li>{{ bullet }}</li>
  {% endfor %}
  </ul>
</article>
{% endfor %}