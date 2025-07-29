---
layout: single
title: "Proyectos"
permalink: /projects/
author_profile: false
---

Aquí encontrarás algunos de los proyectos en los que he trabajado o que estoy desarrollando.

---

{% for project in site.projects %}
### [{{ project.title }}]({{ project.url | relative_url }})
{{ project.excerpt }}
{% endfor %}
