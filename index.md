---
layout: home
title: "Bienvenido"
excerpt: "Portfolio profesional de Roberto Esteban Olivares"
author_profile: true
---


Soy **Roberto Esteban Olivares**, ingeniero informático con especialización en análisis, procesamiento y visualización de datos. Me motiva convertir información compleja en soluciones prácticas que aporten valor real a las organizaciones.

Mi objetivo es seguir desarrollándome profesionalmente en el ámbito del **Data Engineering** y la **Analítica de Datos**, aplicando tecnología para mejorar la eficiencia y la toma de decisiones.

Me considero una persona adaptable, proactiva y con una fuerte orientación al aprendizaje continuo. Disfruto asumir nuevos retos, incorporar herramientas y metodologías actualizadas, y trabajar en entornos colaborativos donde la comunicación y el trabajo en equipo sean pilares clave para alcanzar resultados sobresalientes.

## 🛠️ Herramientas y tecnologías que domino

- **Lenguajes:** Python, SQL, Bash, Java
- **Análisis de datos:** Power BI, Pandas, Seaborn, Scikit-learn, Tableau
- **Bases de datos:** MySQL, MongoDB, SQLite
- **Automatización y DevOps:** Jenkins, Git, Docker
- **IA / NLP:** VADER, BERT, GPT-4, OpenAI API
- **Otros:** Jupyter, FastAPI, VSCode

## 🚀 Últimos proyectos

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects limit:3 %}
- [{{ project.title }}]({{ project.url | relative_url }}): {{ project.excerpt }}
{% endfor %}
