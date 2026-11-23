---
layout: page
title: Research
permalink: /research/
intro: We study how neurotransmitter systems and neural circuits shape brain function and behavior.
---

Our research brings together molecular pharmacology, systems neuroscience, behavioral analysis, and neuroimaging to understand how brain states influence the effects of drugs and the expression of motivated behavior.

## Research themes

{% for item in site.data.research %}
<article class="feature-row">
  {% if item.image %}<img src="{{ item.image | relative_url }}" alt="{{ item.title }}">{% endif %}
  <div>
    <h3>{{ item.title }}</h3>
    <p>{{ item.description }}</p>
  </div>
</article>
{% endfor %}

## How we work

We combine complementary approaches, including receptor pharmacology, behavioral assays, fiber photometry, optogenetic tools, biosensors, and PET imaging. The specific methods used depend on the biological question.
