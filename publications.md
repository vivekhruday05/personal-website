---
layout: page
title: Publications
permalink: /publications/
---

{% assign resume = site.data.resume %}

Research papers, accepted work, and items under review. Each paper includes a searchable external link so the page stays useful even before the final URLs are updated.

{% for paper in resume.publications %}
<article class="list-card publication-card">
  <div class="list-card-head">
    <div>
      <span class="pill">{{ paper.status }}</span>
      <h2>{{ paper.title }}</h2>
      <p class="muted">{{ paper.venue }}</p>
    </div>
    <a class="btn btn-secondary" href="{{ paper.url }}" target="_blank" rel="noreferrer">arXiv / search</a>
  </div>
  <p>{{ paper.summary }}</p>
  <p class="fineprint">{{ paper.impact }}</p>
</article>
{% endfor %}