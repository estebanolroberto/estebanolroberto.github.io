---
title: "Automatización de Atención al Cliente con IA"
excerpt: "Clasificación automática de correos electrónicos, respuestas automáticas, almacenamiento en base de datos y dashboards en tiempo real con reentrenamiento del modelo."
date: 2025-09-12
layout: single
collection: projects
author_profile: false
read_time: true
image: /assets/images/cover-ai-support.png
toc: false
categories:
  - proyectos
tags:
  - inteligencia artificial
  - automatización
  - atención al cliente
  - machine learning
  - fastapi
  - postgres
  - n8n
  - metabase
---

![Portada del proyecto](/assets/images/cover-ai-support.png){: width="100%" }

## 📌 Descripción del proyecto

Este proyecto implementa un sistema de **automatización de atención al cliente** que recibe correos electrónicos de clientes, los **clasifica automáticamente con IA** (pedido, incidencia, consulta, reclamación), responde al cliente, almacena los eventos en **Postgres** y ofrece **dashboards en Metabase**.  

Además, soporta **feedback humano**: los operadores pueden corregir la categoría predicha y esas correcciones se usan para **reentrenar el modelo periódicamente** (MLOps ligero).  

---

## 🔍 Flujo del sistema

1️⃣ **Recepción de correos**  
- n8n conecta con Gmail vía IMAP y recoge los mensajes.  

2️⃣ **Clasificación automática**  
- FastAPI + scikit-learn clasifican los correos en 4 categorías.  

3️⃣ **Almacenamiento**  
- Los resultados se guardan en `events` (Postgres), incluyendo `confidence` y `true_label`.  

4️⃣ **Respuesta automática**  
- n8n envía confirmación al cliente (SMTP → MailHog).  

5️⃣ **Visualización**  
- Metabase muestra métricas como:
  - Distribución de correos por categoría.
  - Confianza media por predicción.

6️⃣ **Corrección humana y retraining**  
- Operadores corrigen `true_label` en Metabase.
- Endpoint `/retrain` de FastAPI actualiza el modelo con los datos corregidos.

---

## 🏗️ Arquitectura

![Arquitectura del sistema](/assets/images/architecture-ai-support.PNG){: width="100%" }
---

## ⚙️ Stack Tecnológico

- **IA/ML**: Python, scikit-learn, FastAPI  
- **Automatización**: n8n  
- **Base de Datos**: PostgreSQL 16  
- **Dashboards**: Metabase  
- **Correo Sandbox**: MailHog  
- **Infraestructura**: Docker Compose  

---

## 📁 Archivos del proyecto

- 📦 `/api` → API con FastAPI + modelo scikit-learn.  
- 📦 `/db/init.sql` → creación de tablas y vistas.  
- 📦 `/n8n` → configuración de workflows.  
- 📦 `/models` → modelo entrenado persistente (`model.joblib`).  

---

## 🎯 Conclusiones

- El sistema **automatiza tareas repetitivas** de soporte.  
- Permite a los agentes centrarse en casos complejos.  
- Integra **IA + automatización + visualización** en un único stack.  
- Gracias al retraining, el modelo **mejora con el tiempo**.  

---
