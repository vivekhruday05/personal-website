---
layout: page
title: Projects
permalink: /projects/
---

{% assign resume = site.data.resume %}

{% for project in resume.projects %}
<article class="list-card project-card">
  <div class="list-card-head">
    <div>
      <h2>{{ project.title }}</h2>
      <p class="muted">{{ project.stack }}</p>
    </div>
  </div>
  <p>{{ project.summary }}</p>
  <ul class="compact-list">
  {% for bullet in project.bullets %}
    <li>{{ bullet }}</li>
  {% endfor %}
  </ul>
</article>
{% endfor %}