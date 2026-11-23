---
layout: page
title: Publications
permalink: /publications/
intro: Selected publications from the Bonaventura Lab and our collaborators.
---

<p class="muted">For a complete and up-to-date record, see our <a href="{{ site.data.links.google_scholar }}">Google Scholar profile</a>.</p>
{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in pubs %}
  {% assign pub_year = pub.year | strip %}
  {% if pub_year != "" and pub_year != current_year %}
    {% assign current_year = pub_year %}
    <h2 class="year-heading">{{ current_year }}</h2>
  {% endif %}
  <article class="publication">
    <h3>{{ pub.title }}</h3>
    <p>{{ pub.authors }}</p>
    <p class="publication-meta">
      <em>{{ pub.journal }}</em>{% if pub.volume %}, {{ pub.volume }}{% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}.{% if pub.type %} <span class="publication-type">{{ pub.type }}</span>{% endif %}
    </p>
    <div class="publication-links">
      {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}">DOI</a>{% endif %}
      {% if pub.pubmed %}<a href="{{ pub.pubmed }}">PubMed</a>{% endif %}
      {% if pub.pdf %}<a href="{{ pub.pdf }}">PDF</a>{% endif %}
      {% if pub.code %}<a href="{{ pub.code }}">Code</a>{% endif %}
    </div>
  </article>
{% endfor %}
