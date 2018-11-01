---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a fourth-year Ph.D student interested in Syntax, Computational Linguistics and Chinese dialects. My interests lie in freedom of word orders. Finished projects on word order include Mandarin SOV derivation and Minimalist parsing of English heavy NP shift (HNPS). Currently, I am working on Japanese long-before-short word order and exploring its connections with HNPS in derivation and parsing. 

**News**

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}