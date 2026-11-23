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
  <a href="{{ member.scholar }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar profile" title="Google Scholar">
    <img src="{{ '/assets/images/gscholar-logo.svg' | relative_url }}" alt="">
  </a>
{% endif %}

  {% if member.website %}
    <a href="{{ member.website }}">Website</a>
  {% endif %}

{% if member.strava %}
  <a href="{{ member.strava }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Strava profile" title="Strava">
    <img src="{{ '/assets/images/strava-logo.svg' | relative_url }}" alt="">
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
  <a href="{{ member.scholar }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar profile" title="Google Scholar">
    <img src="{{ '/assets/images/gscholar-logo.svg' | relative_url }}" alt="">
  </a>
{% endif %}

  {% if member.website %}
    <a href="{{ member.website }}">Website</a>
  {% endif %}

 {% if member.strava %}
  <a href="{{ member.strava }}" class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Strava profile" title="Strava">
    <img src="{{ '/assets/images/strava-logo.svg' | relative_url }}" alt="">
  </a>
{% endif %}
</div>
  </article>
{% endfor %}
</div>
