---
permalink: /program/
title: "Program"
author_profile: true
---
<div>
<embed src="{{ site.baseurl }}/files/ProgrammeWaveTurb_v0.pdf" width="450" height="300" type='application/pdf'> 
</div>

***

## Abstracts
{% for collection in site.collections %}
{% if collection.label == "talks" %}
  {% for post in collection.docs %}
  {% include archive-single.html %}
  {% endfor %}
{% endif %}
{% endfor %}
