---
title: "F1 Qualifying Prediction Model – Las Vegas GP 2025"
excerpt: "Machine learning model trained on real F1 qualifying data (2024–2025). Includes feature engineering, model tuning and a qualifying prediction for the Las Vegas Grand Prix."
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
  - formula 1
  - machine learning
  - xgboost
  - sports analytics
  - python
---

![F1 Logo](/assets/images/f1.jpg){: width="90px" style="float:right; margin-left:10px;" }

### 🏎️ F1 Qualifying Prediction – Las Vegas GP 2025  
📅 Phase 1 completed – November 2025  
💻 Python + FastF1 + XGBoost + Seaborn/Matplotlib  

---

This project builds a machine learning model to predict **Formula 1 qualifying positions** for a Grand Prix.

In this first phase, the goal is to generate a realistic prediction for the **2025 Las Vegas Grand Prix**, using only **historical qualifying data** from the 2024 and 2025 seasons.

---

### 1. Data collection

- Real qualifying sessions loaded with **FastF1**.  
- Seasons used:
  - Full **2024** qualifying data.
  - All **2025** qualifying sessions up to São Paulo (Round 21).
- Variables included: driver abbreviation, team name, Q1/Q2/Q3 times, event name, round and year.

---

### 2. Feature engineering

For every driver and round, several performance features were created:

- `avg_quali_before` – season average position in qualifying (up to the previous round).  
- `last3_avg_before` – average position in the last 3 qualifyings.  
- `trend_before` – short-term form: improvement or decline over recent sessions.  
- `team_avg_before` – average qualifying level of the team.  
- `delta_vs_team` – difference between the driver and the car’s average (negative = outperforming the car).

These features describe both **driver form** and **team strength**.

---

### 3. Model training

Two main model families were evaluated using **XGBoost Regressor**:

#### Model v1 – 5 features  
Uses only form and team features.  
After tuning depth, learning rate and regularization:

- ✅ **Best MAE ≈ 3.37 positions**

#### Model v2 – 7 features  
Adds circuit type and season progress.  
Several variants were tested, but:

- ❌ MAE stayed **worse** than v1 (around 3.55–3.63)  
- ➤ v2 was discarded as the extra features added noise.

**Conclusion:** the simpler **v1** model generalizes better with the available data.

---

### 4. Final prediction – Las Vegas GP 2025

Using the tuned **v1 model**, a full predicted qualifying order was generated for **Las Vegas 2025**, combining:

- 2024 and 2025 historical qualifying form,  
- driver vs. team relative performance,  
- and baseline team pace.

The final predicted grid is summarised in the following chart:

![Las Vegas 2025 Prediction](/assets/images/lasvegas.png)

*Chart exported directly from the notebook and styled with the official 2025 team colours.*

---

### 5. Visual analysis

The Jupyter Notebook also contains supporting visualizations, such as:

- Average qualifying position per driver (2024–2025).  
- Team performance comparison.  
- Scatter plot of long-term form vs. last-3 races form.  
- Bar chart with predicted qualifying order for Las Vegas.

These plots help understand **why** the model predicts a certain grid, rather than treating it as a black box.

---

### 6. Files in the project

- `F1_Qualy_Predictions_Las_Vegas_2025.ipynb` – full notebook with:
  - data loading,  
  - feature engineering,  
  - model training and tuning,  
  - predictions and visualizations.

- `/assets/images/f1.jpg` – project thumbnail (F1 themed).  
- `/assets/images/lasvegas.png` – final qualifying prediction for the Las Vegas GP.

---

### 7. Next steps (future work)

Possible Phase 2 improvements:

- Incorporate **FP1–FP3** pace and sector times as extra features.  
- Analyse ideal laps (best sector combinations).  
- Explore ensemble models and classification-style metrics (e.g. probability of being in Top 5).  
- Add modules for **Safety Car** and **Red Flag** probability based on historical race control messages.  
- Deploy a small web app (Streamlit) or API to generate predictions before each race weekend.

---

📌 **Status:** Phase 1 completed and documented.  
The current version already offers realistic qualifying predictions and a solid base for future F1 analytics experiments.
