---
layout: single
title: "Proyectos"
permalink: /projects/
author_profile: false
---

Aquí encontrarás algunos de los proyectos en los que he trabajado o que estoy desarrollando.

---

<div class="grid__wrapper">

{% for project in site.projects %}
<div class="card__project" style="width: 100%; max-width: 320px; display: inline-block; margin: 1rem; vertical-align: top;">
  <a href="{{ project.url | relative_url }}">
    <img src="{{ project.image | default: '/assets/images/default-project.png' }}" alt="{{ project.title }}" style="width:100%; border-radius: 10px;">
    <h3 style="margin-top: 0.5rem;">{{ project.title }}</h3>
    <p style="margin: 0;">{{ project.excerpt }}</p>
  </a>
</div>
{% endfor %}

</div>
