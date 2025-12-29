---
layout: default
title: Work
permalink: /projekty/
---

{% for project in site.projects %}
  <div style="margin-bottom:80px;">

    {% if project.header.teaser %}
      <a href="{{ project.url | relative_url }}">
        <img
          src="{{ project.header.teaser | relative_url }}"
          alt="{{ project.title }}"
          loading="lazy"
          style="width:100%; display:block; margin-bottom:16px;"
        >
      </a>
    {% endif %}

    <h2 style="margin:0 0 6px 0; text-transform:uppercase;">
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
    </h2>

    {% if project.excerpt %}
      <p style="margin:0;">{{ project.excerpt }}</p>
    {% endif %}

  </div>
{% endfor %}
