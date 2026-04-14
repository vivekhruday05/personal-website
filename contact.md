---
layout: page
title: Contact
permalink: /contact/
---

{% assign resume = site.data.resume %}

The quickest way to reach out is email. The social links are left as editable placeholders so they can be replaced with the final profiles later.

<div class="card-grid cards-2">
  <article class="info-card">
    <span class="card-label">Email</span>
    <strong><a href="mailto:{{ resume.profile.email }}">{{ resume.profile.email }}</a></strong>
    <p>Preferred for academic and collaboration inquiries.</p>
  </article>
  <article class="info-card">
    <span class="card-label">Phone</span>
    <strong><a href="tel:{{ resume.profile.phone | replace: ' ', '' }}">{{ resume.profile.phone }}</a></strong>
    <p>Useful for urgent coordination.</p>
  </article>
</div>

<div class="list-card">
  <h2>Socials</h2>
  <div class="tag-cloud">
  {% for social in resume.profile.socials %}
    {% if social.url and social.url != "" %}
      <a class="tag tag-link" href="{{ social.url }}" target="_blank" rel="noreferrer">{{ social.label }}</a>
    {% else %}
      <span class="tag tag-placeholder">{{ social.label }} · add URL</span>
    {% endif %}
  {% endfor %}
  </div>
</div>