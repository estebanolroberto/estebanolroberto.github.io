---
title: "Análisis de datos con Python: Pandas, NumPy y Matplotlib"
excerpt: "Curso intensivo para dominar las bibliotecas clave del ecosistema Python orientadas al análisis y visualización de datos."
date: 2025-10-29
layout: single
collection: projects
author_profile: false
read_time: true
image: /assets/images/pandas-logo.png
toc: false
categories:
  - formación
tags:
  - pandas
  - numpy
  - matplotlib
  - análisis de datos
  - python
---

![Logo Pandas](/assets/images/pandas-logo.png){: width="90px" style="float:right; margin-left:10px;" }

### 🎓 Curso completado – Udemy  
📅 Finalizado: Junio de 2023  
⏱️ Duración total: 1.5 horas  
⭐ Calificación del curso: 4.5 / 5  
👨‍🏫 Instructor: [Federico Garay](https://www.udemy.com/user/federicogaray/)
📂 Repositorio del proyecto: [🔗 estebanolroberto/Curso-Pandas-Python](https://github.com/estebanolroberto/Curso-Pandas-Python)


---

### 📘 Descripción

Este curso proporcionó una introducción completa y práctica al **análisis de datos con Python**, utilizando las bibliotecas **Pandas**, **NumPy** y **Matplotlib**.  
A través de ejemplos guiados y ejercicios reales, aprendí a manipular, transformar, limpiar y visualizar datos de forma eficiente y profesional.

La formación cubre el flujo completo de trabajo analítico, desde la lectura de datos y la exploración inicial hasta la generación de visualizaciones y la obtención de conclusiones a partir de los datos.

---

### 🧠 Habilidades adquiridas

- Lectura y escritura de archivos CSV, Excel y otros formatos con `pandas`.
- Limpieza, filtrado, indexación y agrupamiento de datos (`groupby`).
- Cálculo de estadísticas descriptivas y análisis exploratorio (EDA).
- Creación de gráficos con `matplotlib` y personalización de ejes, etiquetas y estilos.
- Uso de `numpy` para operaciones numéricas vectorizadas y manejo de arrays.
- Trabajo eficiente con **DataFrames** y **Series**.
- Representación visual de tendencias, distribuciones y relaciones entre variables.

---

### 🧩 Tecnologías utilizadas

| Herramienta | Descripción |
|--------------|-------------|
| **Python 3** | Lenguaje de programación base |
| **Pandas** | Manipulación y análisis de datos estructurados |
| **NumPy** | Cálculo científico y manejo de matrices |
| **Matplotlib** | Visualización y gráficos |
| **Jupyter Notebook** | Entorno interactivo para desarrollo y documentación |

---

### 💻 Ejemplo práctico

```python
import pandas as pd
import matplotlib.pyplot as plt

# Cargar datos
tabla = pd.read_csv('VentasPorProveedor.csv', sep=';')
tabla['Ganancia'] = tabla['Ganancia'].str.replace(',', '.').astype(float)

# Filtrar categoría
alimentos = tabla[tabla['Categoría'] == 'Comestibles']

# Visualización
alimentos['Artículo'].value_counts().plot(kind='bar', figsize=(10,5))
plt.title('Artículos comestibles más vendidos')
plt.xlabel('Artículo')
plt.ylabel('Cantidad')
plt.show()
```

## 👨‍🏫 Instructor

Federico Garay
Instructor Best-Seller en Udemy, con más de 400.000 estudiantes y más de 50 cursos publicados.
Apasionado por enseñar, aprender y compartir conocimientos sobre programación, análisis de datos y productividad digital.

## 🏁 Resultados obtenidos
✔ Manejo fluido de la biblioteca Pandas.

✔ Capacidad para realizar análisis de datos y visualizaciones básicas.

✔ Comprensión sólida del flujo de trabajo analítico con Python.

✔ Mejora de la eficiencia en la manipulación y exploración de datasets.