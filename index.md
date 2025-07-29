---
layout: home
title: "Bienvenido"
excerpt: "Portfolio profesional de Roberto Esteban Olivares"
author_profile: true
---


Soy **Roberto Esteban Olivares**, ingeniero informático especializado en el análisis, procesamiento y visualización de datos. Me apasiona transformar datos complejos en soluciones útiles que generen valor.

En este espacio encontrarás una muestra de mi trayectoria, proyectos y conocimientos en tecnologías como Python, Power BI, SQL, MongoDB y automatización con Jenkins.

Mi objetivo es seguir creciendo profesionalmente en el ámbito del **Data Engineering** y la **Analítica de Datos**, aportando eficiencia y claridad a través de la tecnología.


## 🚀 Últimos proyectos

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects limit:3 %}
- [{{ project.title }}]({{ project.url | relative_url }}): {{ project.excerpt }}
{% endfor %}
