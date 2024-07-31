---
permalink: /program/
title: "Program"
author_profile: true
---
<div>
<embed src="{{ site.baseurl }}/files/ProgrammeWaveTurb_v0.pdf" width="450" height="300" type='application/pdf'> 
</div>

***
{% assign now = 'now' | date: '%s' %}

## Upcoming
{% for collection in site.collections %}
{% if collection.label == "talks" %}
  {% for post in collection.docs %}
    {% assign event_time = post.date | date: '%s' %}
    {% if now < event_time %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}
{% endif %}
{% endfor %}

## Past
{% assign now = 'now' | date: '%s' %}
{% for collection in site.collections %}
{% if collection.label == "talks" %}
  {% for post in collection.docs %}
    {% assign event_time = post.date | date: '%s' %}
    {% if now > event_time %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}
{% endif %}
{% endfor %}