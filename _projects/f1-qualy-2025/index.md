---
title: "Predicción de Clasificación en Fórmula 1 – GP de Las Vegas 2025"
excerpt: "Modelo de machine learning entrenado con datos reales de clasificación (2024–2025) para estimar el rendimiento en el GP de Las Vegas 2025."
date: 2025-11-15
layout: single
collection: projects
author_profile: false
read_time: true
image: /assets/images/f1.jpg
toc: false
categories:
  - proyectos
tags:
  - fórmula 1
  - machine learning
  - modelado predictivo
  - analítica deportiva
  - xgboost
  - python
---

![Logo F1](/assets/images/f1.jpg){: width="110px" style="float:right; margin-left:10px;" }

### 🏎️ Modelo de Predicción de Clasificación – F1  
📅 Fase 1 completada – Noviembre 2025  
💻 Python · FastF1 · XGBoost · Matplotlib  

---

### 📘 Descripción del proyecto

Este proyecto desarrolla un **modelo predictivo** capaz de estimar el resultado de la sesión de **clasificación (Qualy)** de Fórmula 1 para un Gran Premio concreto.

La primera fase se centra en generar una predicción realista para el **GP de Las Vegas 2025**, utilizando exclusivamente los datos oficiales de clasificación de las temporadas **2024 y 2025**.

El análisis completo, visualizaciones, limpieza de datos, ingeniería de características y entrenamiento del modelo están incluidos en el notebook del proyecto.

---

## 🧠 Componentes principales

### 🔹 1. Obtención y consolidación de datos  
Se recopilaron mediante **FastF1** todas las sesiones de clasificación de:

- temporada 2024 completa  
- temporada 2025 hasta el GP de São Paulo (Ronda 21)

Cada sesión incluye: piloto, equipo, tiempos por fase (Q1/Q2/Q3), ronda y año.

---

### 🔹 2. Ingeniería de características  
Se generaron las métricas clave que capturan la forma real de cada piloto:

- `avg_quali_before` → media general de clasificación  
- `last3_avg_before` → forma reciente  
- `trend_before` → tendencia (mejora/empeora)  
- `team_avg_before` → rendimiento medio del monoplaza  
- `delta_vs_team` → diferencia entre piloto y coche  

Estas características demostraron ser las más estables y predictivas.

---

### 🔹 3. Entrenamiento del modelo  
Se probaron dos versiones del modelo:

#### **Modelo v1 (5 variables) – el mejor**
- Precisión final: **MAE = 3.37 posiciones**
- Sencillo, estable y altamente predictivo

#### **Modelo v2 (7 variables)**
- Añadía tipo de circuito y progreso de temporada  
- No mejoró los resultados → descartado  

---

## 📈 Predicción final: GP de Las Vegas 2025

El modelo final genera:

- parrilla de clasificación estimada  
- comparación con el rendimiento histórico  
- análisis por piloto y por equipo  
- visualización completa estilizada con colores oficiales F1 2025

A continuación, la gráfica generada:

![Predicción Las Vegas 2025](/assets/images/lasvegas.png){: width="100%" style="margin-top:20px;" }

---

## 📊 Visualizaciones incluidas en el notebook

- evolución de rendimiento por piloto  
- comparación entre equipos  
- relación forma histórica vs forma reciente  
- parrilla predictiva final  

---

## 📁 Archivos del proyecto

- **Notebook:**  
  `F1_Qualy_Predictions_Las_Vegas_2025.ipynb`

- **Gráficos:**  
  - `/assets/images/lasvegas.png`  
  - gráficos adicionales generados durante el análisis

- **Dataset consolidado:**  
  clasificación 2024–2025 tratada y enriquecida  

---

## 🎯 Objetivo de esta fase

Construir una base sólida que permita predecir la clasificación de cualquier GP usando:

- rendimiento histórico  
- tendencia  
- diferencia piloto–coche  

Esta fase forma el núcleo del sistema de predicción completo.

---

## 🚀 Próximos pasos (Fase 2)

- Integrar tiempos reales de **FP1, FP2 y FP3**  
- Análisis de sectores e “ideal lap”  
- Modelos en conjunto (XGBoost + GradientBoosting + RandomForest)  
- Módulos futuros:
  - probabilidad de Safety Car  
  - riesgo de bandera roja  
- Publicación en **Streamlit** o API ligera para predicción en tiempo real

---

📌 **Estado actual:**  
**Fase 1 finalizada y publicada en GitHub Pages.**
