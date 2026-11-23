---
layout: page
title: Resources
permalink: /resources/
intro: Software, analysis workflows, protocols, and other resources shared by the lab.
---

<div class="resource-grid">
{% for repo in site.data.repositories %}
  <article class="resource-card">
    <p class="eyebrow">{{ repo.type }}</p>
    <h2><a href="{{ repo.url }}">{{ repo.name }}</a></h2>
    <p>{{ repo.description }}</p>
    <div class="publication-links">
      {% if repo.language %}<span>{{ repo.language }}</span>{% endif %}
      {% if repo.doi %}<a href="https://doi.org/{{ repo.doi }}">DOI</a>{% endif %}
      <a href="{{ repo.url }}">GitHub ↗</a>
    </div>
  </article>
{% endfor %}
</div>
