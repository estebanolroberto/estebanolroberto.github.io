---
title: "Análisis de la estancia media en alojamientos rurales (España 2023)"
excerpt: "Exploración y visualización del comportamiento de los viajeros en turismo rural por provincia, mes y procedencia. Proyecto realizado con Python, Machine Learning y Power BI."
date: 2025-08-01
layout: single
collection: projects
author_profile: false
read_time: true
image: /assets/images/cover-rural-data.png
toc: false
categories:
  - proyectos
tags:
  - análisis de datos
  - turismo
  - machine learning
  - power bi
  - visualización
  - python
---

![Portada del proyecto](/assets/images/cover-rural-data.png){: width="100%" }

## 📌 Descripción del proyecto

Este proyecto analiza la estancia media de viajeros en alojamientos rurales por **provincia, procedencia y mes** en España durante 2023. Los datos proceden del **Instituto Nacional de Estadística (INE)** y están disponibles como datos abiertos a través del portal del gobierno:

🔗 [Datos originales](https://datos.gob.es/es/catalogo/ea0010587-estancia-media-de-los-viajeros-por-provincias-procedencia-de-los-viajeros-y-meses-eotr-identificador-api-59642)

---

## 🔍 Fases del análisis

### 1️⃣ Data Collection
- Se utilizó el dataset en formato CSV proporcionado por el INE.
- Separador de columnas: `;`
- Columnas: provincia, procedencia del viajero, mes, estancia media.

### 2️⃣ Data Cleaning & Preparation
- Conversión de campos numéricos (`Total`) a tipo float.
- Eliminación de valores vacíos o totales agregados.
- Renombrado y normalización de columnas.

### 3️⃣ Exploratory Data Analysis (EDA)
#### 🔹 Provincias con mayor y menor estancia media:
- **Mayor estancia**: Castellón (6.24 días)
- **Menor estancia**: A Coruña (1.50 días)

#### 🔹 Diferencias por procedencia:
- **No residentes**: 3.43 días de media
- **Residentes en España**: 2.43 días

#### 🔹 Tendencia mensual nacional:
- **Mes pico**: Agosto (3.85 días)
- **Mes más bajo**: Mayo (2.35 días)

#### 🔹 Agrupación por clusters:
Provincias segmentadas en 5 categorías de estancia: Short, Moderate, Long, Very Long.

### 4️⃣ Feature Engineering
- Codificación de variables categóricas (`province`, `season`, `traveler_origin`)
- Asignación de número de mes (`month_num`)
- Clasificación de la estación del año

### 5️⃣ Modelling
Se entrena un modelo de regresión (`RandomForestRegressor`) para predecir la estancia media a partir de:
- Provincia
- Procedencia del viajero
- Mes
- Estación del año

🔎 Resultados:
- **MAE**: 0.55 días
- **R²**: 0.5852
- Se habilita una función para realizar predicciones individuales en base a inputs definidos.

### 6️⃣ Visualización Power BI

Complementamos el análisis con un dashboard interactivo en Power BI, que permite:
- Comparar procedencias
- Ver tendencias mensuales
- Detectar provincias destacadas
- Observar KPIs clave

📊 Vista del dashboard:

![Dashboard Power BI](/assets/images/dashboardINE.png)

---

## 📁 Archivos del proyecto

Puedes descargar todos los archivos aquí:

- 📓 [Notebook Jupyter (Análisis completo)](/assets/data/ProjectINE_AvgStay.ipynb)
- 📈 [Dashboard Power BI (.pbix)](/assets/data/DashboardAvgStayINE.pbix)
- 🧾 [Dataset original limpio](/assets/data/avg_stay_provinces_clean.csv)

---

## 🎯 Conclusiones finales

- Existe un patrón estacional claro, con **picos de estancia en verano**, especialmente en agosto.
- Las provincias costeras o insulares como **Castellón o Santa Cruz de Tenerife** presentan estancias más largas.
- **Los viajeros extranjeros permanecen más tiempo** que los nacionales, lo cual puede ser relevante para diseñar estrategias turísticas diferenciadas.
- El modelo predictivo ofrece una estimación razonable de la estancia media a partir de variables conocidas.

---

📍 Fuente oficial de datos: [INE](https://datos.gob.es/es/catalogo/ea0010587-estancia-media-de-los-viajeros-por-provincias-procedencia-de-los-viajeros-y-meses-eotr-identificador-api-59642)

