---
layout: page
title: Contact
permalink: /contact/
intro: Get in touch with the Bonaventura Lab.
---

**Bonaventura Lab**  
Department of Pathology and Experimental Therapeutics  
Faculty of Medicine and Health Sciences, University of Barcelona  
Barcelona, Spain

{% if site.data.links.email %}Email: [{{ site.data.links.email }}](mailto:{{ site.data.links.email }}){% endif %}

**Affiliations**  
{% for affiliation in site.data.affiliations %}
- [{{ affiliation.name }}]({{ affiliation.url }})
{% endfor %}
