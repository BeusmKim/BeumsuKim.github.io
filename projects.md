---
layout: default
title: Projects
subtitle: "Selected work — problem framing, implementation, and production considerations"
permalink: /projects
---

{% for p in site.projects %}
<div class="card">
  <strong><a href="{{ p.url | relative_url }}">{{ p.title }}</a></strong><br/>
  <span class="kpi">{{ p.summary }}</span><br/>
  <span class="kpi">Stack: {{ p.stack }}</span>
</div>
{% endfor %}
