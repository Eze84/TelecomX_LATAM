# 📡 Telecom X — Análisis de Evasión de Clientes (Churn)

## 📋 Descripción

Este proyecto forma parte del desafío de Data Science de **Telecom X**, una empresa
que enfrenta una alta tasa de cancelación de clientes. El objetivo es recopilar,
procesar y analizar los datos de clientes para identificar los factores que impulsan
la evasión, proporcionando insights accionables al equipo de Data Science para el
desarrollo de modelos predictivos y estrategias de retención.

---

## 🎯 Objetivos

- Extraer datos desde una API en formato JSON
- Aplicar técnicas de ETL para limpiar y transformar los datos
- Realizar un Análisis Exploratorio de Datos (EDA)
- Identificar patrones y factores asociados al churn
- Generar conclusiones y recomendaciones estratégicas

---

## 🗂️ Estructura del Proyecto
```
telecomx-churn/
│
├── TelecomX_Analisis_Churn.ipynb   # Notebook principal con todo el análisis
└── README.md                        # Este archivo
```

---

## 🔄 Etapas del Análisis

### 1. Extracción de Datos
Los datos fueron obtenidos desde una API pública en formato JSON con estructura
anidada y normalizados con `pd.json_normalize()`.

### 2. Limpieza y Transformación
| Problema | Solución aplicada |
|---|---|
| `Charges_Total` en formato string | Conversión a `float` |
| Valores nulos en `Charges_Total` | Imputación con `0` |
| `Churn` en formato Yes/No | Conversión a binario 1/0 |
| Categorías inconsistentes | Unificadas como `"No"` |

### 3. Análisis Exploratorio (EDA)
- Distribución general del churn
- Churn por variables categóricas (contrato, pago, internet, demografía)
- Churn por variables numéricas (tenure, cargos mensuales y totales)
- Mapa de correlaciones

---

## 💡 Principales Hallazgos

- **26.6%** de los clientes canceló el servicio
- Contratos **mes a mes** → ~42% de churn (factor más crítico)
- Clientes **Fiber Optic** presentan la mayor tasa de evasión pese a ser el servicio premium
- Pago por **electronic check** → ~45% de churn
- El riesgo es máximo en los primeros **12 meses** de servicio
- **Adultos mayores** tienen el doble de tasa de churn que el resto
- La adopción de servicios adicionales actúa como **factor protector**

---

## 🚀 Recomendaciones

1. Incentivar la migración de contratos mensuales a anuales
2. Auditar la experiencia del servicio Fiber Optic
3. Promover el débito automático como método de pago
4. Implementar un programa de onboarding en los primeros 12 meses
5. Diseñar planes especiales para adultos mayores
6. Ofrecer bundles con servicios adicionales desde el inicio

---

## 🛠️ Tecnologías Utilizadas

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-teal)
![Colab](https://img.shields.io/badge/Google%20Colab-notebook-yellow?logo=googlecolab)

---

## ▶️ Cómo ejecutar

1. Abrí el notebook en Google Colab
2. Ejecutá las celdas en orden
3. Los datos se cargan automáticamente desde la API — no se requiere ningún archivo local

---

## 👤 Autor

Desarrollado como parte del programa de formación en Data Science — Alura LATAM.
