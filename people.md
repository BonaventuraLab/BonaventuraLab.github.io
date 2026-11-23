---
layout: page
title: People
permalink: /people/
intro: Meet the researchers and students behind our work.
---

<div class="people-grid">
{% assign members = site.data.members | sort: "order" %}
{% for member in members %}
  <article class="person-card">
    {% if member.photo %}
      <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}" class="person-photo">
    {% else %}
      <div class="person-placeholder" aria-hidden="true">{{ member.initials }}</div>
    {% endif %}
    <h3>{{ member.name }}</h3>
    <p class="muted">{{ member.role }}</p>
    {% if member.bio %}<p>{{ member.bio }}</p>{% endif %}
    <div class="person-links">
      {% if member.orcid %}<a href="{{ member.orcid }}">ORCID</a>{% endif %}
      {% if member.scholar %}<a href="{{ member.scholar }}">Google Scholar</a>{% endif %}
      {% if member.website %}<a href="{{ member.website }}">Website</a>{% endif %}
    </div>
  </article>
{% endfor %}
</div>

## Alumni

We are grateful to all former members and collaborators who have contributed to the lab.

<div class="people-grid">
{% assign alumni = site.data.members.alumni | sort: "order" %}
{% for member in alumni %}
  <article class="person-card">
    {% if member.photo %}
      <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}" class="person-photo">
    {% else %}
      <div class="person-placeholder" aria-hidden="true">{{ member.initials }}</div>
    {% endif %}
    <h3>{{ member.name }}</h3>
    <p class="muted">{{ member.role }}</p>
    {% if member.bio %}<p>{{ member.bio }}</p>{% endif %}
    <div class="person-links">
      {% if member.orcid %}<a href="{{ member.orcid }}">ORCID</a>{% endif %}
      {% if member.scholar %}<a href="{{ member.scholar }}">Google Scholar</a>{% endif %}
      {% if member.website %}<a href="{{ member.website }}">Website</a>{% endif %}
    </div>
  </article>
{% endfor %}
</div>
