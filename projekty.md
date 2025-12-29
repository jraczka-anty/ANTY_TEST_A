---
layout: default
title: Work
permalink: /projekty/
---

{% if project.header.teaser %}
<a href="{{ project.url | relative_url }}">
  <img
    src="{{ project.header.teaser | relative_url }}"
    alt="{{ project.title }}"
    loading="lazy"
    style="
      width: 100%;
      max-width: 900px;
      display: block;
      margin-bottom: 24px;
    "
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
