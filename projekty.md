---
layout: default
title: Work
permalink: /projekty/
---

{% for project in site.projects %}
  <div style="max-width:900px; margin:0 auto 72px auto; padding-bottom:48px; border-bottom:1px solid rgba(255,255,255,0.08);">

    {% if project.header.teaser %}
      <a href="{{ project.url | relative_url }}" style="display:block; margin-bottom:22px;">
        <img
          src="{{ project.header.teaser | relative_url }}"
          alt="{{ project.title }}"
          loading="lazy"
          style="
            width:100%;
            display:block;
            border-radius:18px;
          "
        >
      </a>
    {% endif %}

    <h2 style="margin:0 0 10px 0; text-transform:uppercase; letter-spacing:0.04em;">
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
    </h2>

    {% if project.excerpt %}
      <p style="margin:0; opacity:0.92; max-width:58ch;">
        {{ project.excerpt }}
      </p>
    {% endif %}

  </div>
{% endfor %}
