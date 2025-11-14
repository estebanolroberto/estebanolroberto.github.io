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
  - proyectos
tags:
  - fórmula 1
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

This project builds a machine learning model capable of predicting **Formula 1 qualifying positions** for a given Grand Prix.  
The goal of this first phase is to produce a realistic prediction for the **2025 Las Vegas Grand Prix**, using only **historical qualifying data** from 2024 and 2025.

---

## 🧠 Key Components of the Project

### **1. Data Acquisition & Consolidation**
Real qualifying data was obtained via **FastF1**, including:

- all qualifying sessions from the **2024** season  
- all available qualifying sessions from **2025** up to São Paulo (Round 21)

Each session includes: driver abbreviation, team name, Q1/Q2/Q3 times, event name, round, and year.

---

### **2. Feature Engineering**
Key form metrics generated for each driver:

- `avg_quali_before` → season qualifying average  
- `last3_avg_before` → trend in recent performance  
- `trend_before` → short-term improvement/decline  
- `team_avg_before` → team-level performance  
- `delta_vs_team` → driver deviation from car capability  

---

### **3. Model Training**
Two major versions were evaluated:

#### **Model v1 (5 features)**  
✔ Best-performing model  
📉 **Final tuned MAE: 3.37 positions**

#### **Model v2 (7 features)**  
Adds circuit type + season progress  
❌ Did not improve accuracy → discarded  

---

## 📈 Final Prediction – Las Vegas GP 2025

Using the best-tuned version of Model v1, the system generates:

- predicted qualifying order  
- performance indicators for each driver  
- comparison vs Las Vegas 2024  
- fully styled visualizations using official 2025 team colors  

Below is the **final qualifying prediction chart for Las Vegas 2025**:

![Las Vegas 2025 Prediction](/assets/images/lasvegas.png){: width="100%" style="margin-top:20px; border-radius:8px;" }

*Generated automatically from the model using XGBoost and performance-based features.*

---

## 📊 Additional Visualizations Included in the Notebook
- Average qualifying position (2024–2025) per driver  
- Team performance comparison  
- Driver form scatterplot (historical vs last-3)  
- Predicted grid visualization with official team palette  

---

## 📁 Included Project Files

- **Notebook:**  
  `F1_Qualy_Predictions_Las_Vegas_2025.ipynb`
- **Figures:**  
  - `/assets/images/lasvegas.png` (prediction chart)  
  - Additional analytic plots exported from the notebook  
- **Dataset:** consolidated qualifying dataset for 2024–2025  

---

## 🎯 Objective

Create a robust machine learning framework to predict Formula 1 qualifying performance based on **historical form**, **trend**, and **team strength**.

The project lays the groundwork for significantly more powerful models in future phases.

---

## 🚀 Next Steps (Phase 2)

- Integration of FP1–FP3 performance data  
- Sector-time analysis & ideal lap calculations  
- Ensemble models (XGB + GradientBoosting + Random Forest)  
- Predictive modules for:
  - Safety Car probability  
  - Red flag likelihood  
- Deployment as a Streamlit app or lightweight prediction API  

---

📌 **Current Status:**  
**Phase 1 completed and published on GitHub Pages.**
