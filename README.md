Título: Customer Health & Churn Intelligence System
Problema: muchas empresas pierden ingresos por churn silencioso.
Objetivo: construir un sistema que:

cuantifique salud del cliente,

detecte riesgo de churn,

priorice acciones,

estime impacto económico.

Outputs:

Data model en Star Schema (Postgres)

Pipeline reproducible (Python)

Dashboard ejecutivo (Power BI)

Modelo predictivo de churn (baseline + mejorado)

KPIs: churn rate, retention, ARPU/Revenue proxy, cohort retention, health score, expected revenue at risk.

Audiencia: liderazgo comercial / growth / customer success.


customer-health-intelligence/
  data/
    raw/            # aquí pones el csv original (o link, mejor)
    processed/
  sql/
    01_schema.sql
    02_staging.sql
    03_dimensions.sql
    04_facts.sql
  notebooks/
    01_eda.ipynb
  src/
    config.py
    extract_load.py
  dashboard/
    screenshots/
  docs/
    star_schema.png
    storytelling_outline.md
  README.md


