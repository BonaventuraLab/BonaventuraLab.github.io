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
          <span class="bio-text">{{ member.bio }}</span>
          <span class="bio-toggle bio-more">Read more ↓</span>
          <span class="bio-toggle bio-less">Show less ↑</span>
        </summary>
      </details>
    {% endif %}
<div class="person-links">
  {% if member.orcid %}
    <a href="{{ member.orcid }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="ORCID profile" title="ORCID">
      <img src="{{ '/assets/images/orcid-logo.svg' | relative_url }}" alt="">
    </a>
  {% endif %}

  {% if member.scholar %}
    <a href="{{ member.scholar }}">Google Scholar</a>
  {% endif %}

  {% if member.website %}
    <a href="{{ member.website }}">Website</a>
  {% endif %}

{% if member.strava %}
  <a href="{{ member.strava }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Strava profile" title="Strava">
    <svg class="strava-icon" viewBox="0 0 24 24" aria-hidden="true">
      <path fill="#FC4C02" d="M15.3 14.2 12.1 8.1H8.9L2.5 20.4h6.4l1.6-3.1-1.6-3.1H7.3l3.2-6.1 3.2 6.1h-3.2l-1.6 3.1h6.4l1.6-3.1z"/>
      <path fill="#FC4C02" d="m18.5 14.2-1.6 3.1h-3.2l1.6 3.1h3.2l3.2-6.2z"/>
    </svg>
  </a>
{% endif %}
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
          <span class="bio-text">{{ member.bio }}</span>
          <span class="bio-toggle bio-more">Read more ↓</span>
          <span class="bio-toggle bio-less">Show less ↑</span>
        </summary>
      </details>
    {% endif %}
<div class="person-links">
  {% if member.orcid %}
    <a href="{{ member.orcid }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="ORCID profile" title="ORCID">
      <img src="{{ '/assets/images/orcid-logo.svg' | relative_url }}" alt="">
    </a>
  {% endif %}

  {% if member.scholar %}
    <a href="{{ member.scholar }}">Google Scholar</a>
  {% endif %}

  {% if member.website %}
    <a href="{{ member.website }}">Website</a>
  {% endif %}

 {% if member.strava %}
  <a href="{{ member.strava }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Strava profile" title="Strava">
    <svg class="strava-icon" viewBox="0 0 24 24" aria-hidden="true">
      <path fill="#FC4C02" d="M15.3 14.2 12.1 8.1H8.9L2.5 20.4h6.4l1.6-3.1-1.6-3.1H7.3l3.2-6.1 3.2 6.1h-3.2l-1.6 3.1h6.4l1.6-3.1z"/>
      <path fill="#FC4C02" d="m18.5 14.2-1.6 3.1h-3.2l1.6 3.1h3.2l3.2-6.2z"/>
    </svg>
  </a>
{% endif %}
</div>
  </article>
{% endfor %}
</div>
