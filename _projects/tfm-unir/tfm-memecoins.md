---
title: "Predicción de la volatilidad de Memecoins con análisis emocional"
excerpt: "TFM en Visual Analytics centrado en analizar sentimiento y predecir la volatilidad de criptomonedas tipo Memecoins usando series temporales."
date: 2025-07-29
layout: single
collection: projects
author_profile: false
read_time: true
toc: false
categories:
  - proyectos
tags:
  - TFM
  - análisis de sentimiento
  - series temporales
  - memecoins
  - big data
---

![Logo UNIR](/assets/images/unir-logo.png){: width="100px" style="float:right; margin-left:10px;" }

### 📘 Trabajo Final de Máster – UNIR  
📅 En curso – Defensa prevista: Octubre 2025  
🎓 Máster Universitario en Visual Analytics & Big Data

---

Tras meses de trabajo junto a mi compañero **Sergio Díaz de la Peña**, hemos depositado oficialmente nuestro Trabajo Final de Máster titulado:

> **“Predicción de la volatilidad de Memecoins mediante análisis emocional y modelos de series temporales”**

Este proyecto representa una excelente oportunidad para aplicar de forma integrada los conocimientos adquiridos durante el máster, combinando **Data Science**, **Big Data**, **análisis de sentimiento** y **modelado predictivo** con series temporales, todo dentro de un dominio desafiante como el de las criptomonedas de tipo "memecoin".

---

### 🧠 Componentes clave del proyecto

- **Recopilación de datos** desde la API oficial de Reddit, obteniendo publicaciones y comentarios en subreddits relacionados con criptomonedas. Se aplicaron filtros temáticos y temporales para asegurar relevancia y calidad del contenido. Los datos financieros se obtuvieron de la API de **CoinGecko**, incluyendo precios históricos, volumen y volatilidad de memecoins seleccionadas.
  
- **Análisis de sentimiento** mediante una comparativa entre tres enfoques:  
  - **VADER** como modelo léxico de referencia para textos cortos.  
  - **BERT** preentrenado y ajustado para tareas de clasificación de sentimiento.  
  - **GPT-4** a través de **OpenAI API**, aplicando prompts optimizados para obtener interpretaciones emocionales más contextuales.  
  Se comparó la precisión, coherencia y aplicabilidad de los modelos en el contexto de publicaciones sociales.

- **Preprocesamiento y etiquetado de emociones**, incluyendo normalización de texto, eliminación de ruido, lematización y detección de entidades clave. Se clasificaron las emociones predominantes (positiva, negativa, neutra) y se cuantificaron variables como polaridad y subjetividad, conectándolas con los movimientos del mercado.

- **Modelado de series temporales** con el objetivo de predecir la volatilidad futura:
  - Implementación de redes neuronales **LSTM**, entrenadas sobre ventanas de sentimiento y métricas de mercado.  
  - Uso de **Random Forest Regressor** para estimar valores de volatilidad a corto plazo, basándose en características derivadas del análisis emocional.

- **Evaluación de correlación** mediante análisis estadístico clásico (Pearson, Spearman) y visualizaciones que muestran cómo las variaciones en el sentimiento preceden a cambios de comportamiento en las memecoins. Se analizaron patrones y ventanas temporales óptimas para anticipación.

- **Visualización de resultados** a través de dashboards dinámicos en **Power BI**, mostrando predicciones, fluctuaciones emocionales, análisis comparativo de modelos y gráficos temporales interactivos. Se complementó con visualizaciones técnicas detalladas usando `matplotlib`, `seaborn` y `plotly` para documentación y análisis exploratorio.


### 🎯 Objetivo del proyecto

Determinar si existe una relación significativa entre las fluctuaciones emocionales expresadas en redes sociales y la volatilidad observada en el mercado de **memecoins** como Dogecoin, Shiba Inu o PepeCoin. Con ello, se busca:
- Proporcionar alertas tempranas ante posibles cambios bruscos de precio.
- Ofrecer una herramienta complementaria de análisis para traders o investigadores.

---

📌 Estado actual del proyecto:  
Proyecto depositado y en **fase de revisión académica previa a defensa**. La exposición final está prevista para **octubre de 2025**.
