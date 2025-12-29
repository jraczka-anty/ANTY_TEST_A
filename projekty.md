---
layout: default
title: Work
permalink: /projekty/
---

<div style="max-width:760px; margin:0 auto 80px auto;">
  <h1 style="margin:0 0 16px 0; text-transform:uppercase; letter-spacing:0.08em;">
    Nasza droga
  </h1>
  <p style="margin:0; opacity:0.85;">
    Od ram rowerowych po mobilne projekty. Wszystko zaczyna się w ruchu.
  </p>
</div>

{% for project in site.projects %}
  <div style="max-width: 760px; margin: 0 auto 64px auto;">

    {% if project.header.teaser %}
      <a href="{{ project.url | relative_url }}">
        <img
          src="{{ project.header.teaser | relative_url }}"
          alt="{{ project.title }}"
          loading="lazy"
          style="width:100%; display:block; border-radius:12px; margin-bottom:16px;"
        >
      </a>
    {% endif %}

    <h2 style="margin:0 0 8px 0; text-transform:uppercase; letter-spacing:0.06em;">
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
    </h2>

    {% if project.excerpt %}
      <p style="margin:0; opacity:0.9;">{{ project.excerpt }}</p>
    {% endif %}

  </div>
{% endfor %}
