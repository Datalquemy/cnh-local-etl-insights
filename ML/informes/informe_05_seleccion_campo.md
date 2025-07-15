
# 🧠 Informe Técnico – Selección de Candidato para Modelado Predictivo (CNH)

**Archivo fuente del análisis:** `05_cnh_ml_candidate_selection.ipynb`  
**Proyecto:** Predicción de Producción Petrolera – CNH  
**Autor:** Emmanuel Pérez - DatAlquemy  
**Fecha:** Julio 2025  

---

## 🎯 Objetivo del Análisis

Identificar el campo petrolero más estratégico para aplicar Machine Learning, utilizando datos históricos de producción proporcionados por la CNH. El análisis se enfocó en definir qué activo representa mejor un caso de negocio relevante para modelar.

---

## 🧠 Metodología

### 1. Problem Framing (Enmarcado del problema)
Se planteó la pregunta de negocio:  
**“¿Qué campo petrolero es más adecuado para modelar su comportamiento de producción futura?”**

### 2. Análisis de Tendencia con Regresión Lineal
Se aplicó un modelo de regresión lineal simple para calcular la **pendiente mensual de producción** en los 10 campos con mayor volumen acumulado entre 2016 y 2024.  
Esto permitió identificar si cada campo presenta crecimiento, estabilidad o declive.

- Variable independiente: `meses_desde_inicio`
- Variable dependiente: `petroleo_mbd`
- Técnica: `LinearRegression()` de `sklearn`

---

## 📊 Hallazgos Principales

| Campo     | Característica Principal                        |
|-----------|-------------------------------------------------|
| **MALOOB** | Mayor volumen acumulado, tendencia negativa     |
| **AYATSIL** | Pendiente más positiva, fuerte crecimiento     |
| **AKAL**   | Campo histórico, pero en declive                |

> 🔍 **Ayatsil** fue identificado como el mejor candidato para modelado de crecimiento.

---

## 📈 Visualización

Se generó un gráfico de líneas personalizado, con estilos accesibles para daltonismo, que muestra la evolución mensual de producción para los tres campos clave. Esto validó visualmente las tendencias identificadas por el modelo.

---

## ✅ Conclusión

Este análisis concluye la etapa de **selección estratégica del objetivo de modelado**, habilitando el siguiente paso del pipeline de Machine Learning: la preparación del dataset específico y el entrenamiento del modelo predictivo sobre el campo **Ayatsil**.

---
