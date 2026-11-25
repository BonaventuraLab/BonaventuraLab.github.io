
---
layout: page
title: News
permalink: /news/
intro: Updates, publications, events, and life in the lab.
---

<div class="news-list">
{% for post in site.posts %}
  <article class="news-item">
    {% if post.image %}
      <a href="{{ post.url | relative_url }}" class="news-item-image-link">
        <img src="{{ post.image | relative_url }}" alt="{{ post.image_alt | default: post.title | strip_html | escape }}" class="news-item-image">
      </a>
    {% endif %}
    <p class="eyebrow">{{ post.date | date: "%d %B %Y" }}{% if post.category %} · {{ post.category }}{% endif %}</p>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt | strip_html | strip_newlines }}</p>
    <a class="text-link" href="{{ post.url | relative_url }}">Read more →</a>
  </article>
{% else %}
  <p>News from the lab will appear here. Add a Markdown file to <code>_posts</code> to publish an update.</p>
{% endfor %}
</div>
