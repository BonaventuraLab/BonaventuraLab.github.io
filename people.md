
---
layout: page
title: People
permalink: /people/
intro: Meet the researchers and students behind our work.
---

<div class="people-grid">
{% assign members = site.data.members.members | sort: "order" %}
{% for member in members %}
  <article class="person-card">
    {% if member.photo %}
      <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}" class="person-photo">
    {% else %}
      <div class="person-placeholder" aria-hidden="true">{{ member.initials }}</div>
    {% endif %}
    <h3>{{ member.name }}</h3>
    <p class="muted">{{ member.role }}</p>
    {% if member.bio %}
      <details class="person-bio">
        <summary>
          <span class="bio-preview">{{ member.bio }}</span>
          <span class="bio-toggle bio-more">Read more ↓</span>
          <span class="bio-toggle bio-less">Show less ↑</span>
        </summary>
        <div class="bio-full">{{ member.bio }}</div>
      </details>
    {% endif %}
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
    {% if member.bio %}
      <details class="person-bio">
        <summary>
          <span class="bio-preview">{{ member.bio }}</span>
          <span class="bio-toggle bio-more">Read more ↓</span>
          <span class="bio-toggle bio-less">Show less ↑</span>
        </summary>
        <div class="bio-full">{{ member.bio }}</div>
      </details>
    {% endif %}
    <div class="person-links">
      {% if member.orcid %}<a href="{{ member.orcid }}">ORCID</a>{% endif %}
      {% if member.scholar %}<a href="{{ member.scholar }}">Google Scholar</a>{% endif %}
      {% if member.website %}<a href="{{ member.website }}">Website</a>{% endif %}
    </div>
  </article>
{% endfor %}
</div>
