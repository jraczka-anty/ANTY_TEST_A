---
layout: default
title: Work
---

{% for project in site.projects %}
<div style="margin-bottom:80px;">

  {% if project.header.teaser %}
  <a href="{{ project.url }}">
    <img 
      src="{{ project.header.teaser | relative_url }}" 
      alt="{{ project.title }}" 
      loading="lazy"
      style="width:100%; margin-bottom:20px;"
    >
  </a>
  {% endif %}

  <h2 style="margin-bottom:8px;">
    <a href="{{ project.url }}">{{ project.title }}</a>
  </h2>

  <p>{{ project.excerpt }}</p>

</div>
{% endfor %}
