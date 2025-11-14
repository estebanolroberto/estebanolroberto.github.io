---
title: "F1 Qualifying Prediction Model – Las Vegas GP 2025"
excerpt: "Machine learning model trained on real F1 qualifying data (2024–2025). Includes feature engineering, exploratory analysis, XGBoost tuning, and predictive insights for the Las Vegas GP."
date: 2025-11-15
layout: single
collection: projects
author_profile: false
read_time: true
image: /assets/images/f1.jpg
toc: false
categories:
  - projects
tags:
  - formula 1
  - machine learning
  - predictive modeling
  - sports analytics
  - xgboost
  - python
---

![F1 Logo](/assets/images/f1.jpg){: width="120px" style="float:right; margin-left:10px;" }

### 🏎️ F1 Qualifying Prediction – Las Vegas GP 2025  
📅 Phase 1 Completed – November 2025  
💻 Python + FastF1 + XGBoost + Seaborn/Matplotlib  


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
