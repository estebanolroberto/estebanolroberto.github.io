---
title: "Análisis de consumo en una cafetería con visualización en Power BI"
excerpt: "Proyecto de analítica completa aplicado a las ventas de una cafetería. Incluye análisis exploratorio, modelos predictivos y dashboards interactivos en Power BI."
date: 2025-07-30
layout: single
collection: projects
author_profile: false
read_time: true
image: /assets/images/coffe-logo.png
toc: false
categories:
  - proyectos
tags:
  - análisis de datos
  - visualización
  - power bi
  - machine learning
  - clustering
  - python
---

![Logo Café](/assets/images/coffe-logo.png){: width="100px" style="float:right; margin-left:10px;" }

### 📊 Proyecto de análisis de datos y visualización interactiva  
📅 Finalizado – Julio 2025  
💻 Proyecto individual en entorno Python + Power BI

---

Este proyecto explora el comportamiento de clientes en una **cafetería de Ciudad del Cabo** mediante el análisis de transacciones realizadas durante el mes de marzo de 2024. Se aplicó una metodología completa: desde la limpieza y exploración de datos hasta el modelado predictivo y segmentación de perfiles de consumo.

---

### 🧠 Componentes clave del proyecto

- **Exploración de datos (EDA):** análisis de los cafés más vendidos, franjas horarias de mayor actividad, ingresos por día de la semana y ticket medio por tipo de cliente.  
  Se detectaron patrones claros como el pico de consumo a las 10:00 y una alta fidelidad hacia productos como *"Americano with Milk"* y *Latte*.

- **Limpieza y enriquecimiento del dataset**, añadiendo variables como:
  - `is_weekend`: si la compra fue en fin de semana
  - `day_block`: tramo horario (mañana, tarde, noche)
  - `customer_type`: cliente identificado o anónimo
  - `is_outlier`: detección de transacciones anómalas (no se detectaron)

- **Modelos aplicados:**
  - 🔢 **Clasificación:** predicción del método de pago (`cash_type`) con precisión del 100% utilizando Random Forest.
  - 💰 **Regresión:** estimación del valor de una compra (`money`) con un R² de 0.86 y error absoluto medio de solo ZAR 1.34.
  - 🧩 **Clustering:** agrupación de perfiles de consumo mediante KMeans, detectando 4 clusters con comportamientos diferenciados por ticket medio y hora de compra.

- **Exportación del dataset enriquecido y visualización externa con Power BI**, permitiendo una exploración interactiva de todos los hallazgos clave del análisis.

---

### 📁 Recursos incluidos

En esta misma carpeta del repositorio GitHub puedes encontrar:

- [`coffee_transactions_final.csv`](/_projects/project-coffe/coffee_transactions_final.csv): dataset final procesado y enriquecido con todas las variables usadas para el modelado y visualización.
- [`DashboardCoffeShop.pbix`](/_projects/project-coffe/DashboardCoffeShop.pbix): fichero de Power BI con los 5 dashboards interactivos construidos para explorar ventas, productos, clientes, tiempo y clusters.
- [`ProjectCoffe.ipynb`](/_projects/project-coffe/ProjectCoffe.ipynb): notebook de Jupyter completo con todos los pasos del análisis, limpieza, modelado y exportación de datos.

---

### 🎯 Objetivo del proyecto

Extraer valor comercial real a partir de un simple conjunto de transacciones de cafetería, generando:
- Insights sobre hábitos de consumo.
- Clasificación de clientes por comportamiento.
- Visualización ejecutiva y operativa para toma de decisiones.

Este proyecto demuestra cómo, con una buena base de análisis de datos y visualización, se puede transformar información transaccional en decisiones accionables.

---

📌 Estado actual:  
Proyecto finalizado y publicado en entorno GitHub Pages.
