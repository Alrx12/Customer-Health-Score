# Customer Health Score (CHS) – Churn Intelligence System

## Resumen Ejecutivo (Executive Summary)
Muchas empresas pierden ingresos por churn silencioso: clientes que dejan de comprar/usar un servicio sin avisar.  
Este proyecto construye un sistema end-to-end para **medir salud del cliente**, **predecir riesgo de churn**, **priorizar acciones**, y **estimar impacto económico** de intervenir.

Aplicable a cualquier industria con datos transaccionales: retail, e-commerce, telecom, fintech, suscripciones, etc.

---

## Objetivo de Negocio
Construir un **Customer Health Score** y un modelo de churn usando datos transaccionales, para responder:

1) ¿Cómo evoluciona la retención y el revenue?  
2) ¿Qué segmentos y clientes están en riesgo?  
3) ¿Qué acciones priorizar y cuánto dinero está en riesgo?

---

## Definición de Churn (sin fuga de información)
- **Ventana de observación:** 12 meses (para construir features)
- **Ventana de evaluación:** 90 días posteriores al cierre de la observación

Un cliente se marca como churn si:
> No registra actividad (transacción) durante los 90 días de evaluación después del cierre de la ventana de observación.

Esto garantiza consistencia temporal y evita data leakage.

---

## Arquitectura (Stack)
- **PostgreSQL:** modelo dimensional (Star Schema) + capa analítica
- **Python:** EDA, feature engineering, entrenamiento y scoring
- **Power BI:** dashboard ejecutivo con storytelling y simulación de impacto
- **Git/GitHub:** control de versiones y portafolio reproducible

---

## KPIs clave
- Churn rate / retention rate
- Cohort retention
- Revenue at risk (proxy)
- Customer Health Score
- Drivers de churn (features explicativas)
- Impacto estimado de intervención (escenarios)

---

## Dataset
**Online Retail II / E-commerce transactions**  
> Nota: el dataset no se incluye en el repo por tamaño/licencia. Se documenta el origen y se cargará en `data/raw/`.

---

## Estructura del repositorio
```text
Customer-Health-Score/
├── data/
│   ├── raw/
│   └── processed/
├── sql/
│   ├── 01_schema.sql
│   ├── 02_staging.sql
│   ├── 03_dimensions.sql
│   └── 04_facts.sql
├── notebooks/
│   └── 01_eda.ipynb
├── src/
│   ├── config.py
│   └── extract_load.py
├── dashboard/
│   └── screenshots/
└── docs/
    ├── star_schema.png
    └── storytelling_outline.md
