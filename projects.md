---
layout: default
title: Projects
subtitle: "Selected work — problem framing, implementation, and production considerations"
permalink: /projects
---

<div class="grid">
{% for p in site.projects %}
  <a class="project-tile" href="{{ p.url | relative_url }}">
    {% if p.image %}
      <div class="project-thumb"><img src="{{ p.image | relative_url }}" alt="{{ p.title }} thumbnail" /></div>
    {% else %}
      <div class="project-thumb placeholder">No image</div>
    {% endif %}

    <div>
      <div class="project-title">{{ p.title }}</div>
      <div class="kpi">{{ p.summary }}</div>
      <div class="kpi">Stack: {{ p.stack }}</div>
    </div>
  </a>
{% endfor %}
</div>
