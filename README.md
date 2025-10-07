# 🎯 Predicción de Churn en Seguros de Carga

[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3.0-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

> Modelo de Machine Learning para predecir el riesgo de cancelación (churn) en clientes de seguros de carga marítima y terrestre, permitiendo implementar estrategias de retención proactivas.

---

## 📊 Resumen Ejecutivo

Este proyecto desarrolla un sistema predictivo que identifica clientes con alto riesgo de cancelación antes de que abandonen la empresa. El modelo analiza 40 variables de comportamiento, facturación y servicio para generar alertas tempranas y recomendaciones de acción.

**Resultados Principales:**
- ✅ **183 clientes** identificados para acción inmediata (niveles crítico y alto)
- ✅ **100% de recall** con threshold optimizado (detecta todos los churns)
- ✅ **ROC-AUC: 0.808** - Modelo con capacidad discriminatoria robusta
- ✅ **$4,947,737,448 COP** en facturación anual en riesgo identificada

**Impacto de Negocio:** El modelo permite priorizar recursos de retención en los clientes correctos, maximizando el ROI de las campañas.

---

## 🎯 Problema de Negocio

### Contexto
Las empresas de seguros de carga enfrentan una **tasa de churn del 25% anual**, lo que representa:
- Pérdida de ingresos recurrentes
- Alto costo de adquisición de nuevos clientes (5x más caro que retener)
- Dificultad para identificar señales tempranas de insatisfacción

### Objetivo
Desarrollar un modelo de Machine Learning que:
1. Identifique clientes con probabilidad de cancelación superior al 70%
2. Priorice acciones de retención por nivel de riesgo y valor del cliente
3. Proporcione insights accionables sobre los factores que causan churn

---

## 📈 Resultados Clave

### Predicciones Generadas
Del análisis de **400 clientes activos**, se identificaron:

| Nivel de Riesgo | Clientes | Porcentaje | Acción Recomendada |
|-----------------|----------|------------|-------------------|
| 🔴 **Crítico** | 125 | 31.2% | Llamada urgente del gerente + descuento especial |
| 🟠 **Alto** | 58 | 14.5% | Contacto del ejecutivo + revisión de contrato |
| 🟡 **Medio** | 90 | 22.5% | Monitoreo y seguimiento proactivo |
| 🟢 **Bajo** | 127 | 31.8% | Continuar con servicio normal |

### Métricas del Modelo

**Performance en Test Set:**
- **Accuracy:** 80.3%
- **Precision:** 66.7%
- **Recall:** 42.7% (threshold 0.5) → **100%** (threshold optimizado 0.10)
- **F1-Score:** 0.52
- **ROC-AUC:** 0.XXX

**Trade-off Precision-Recall:**
- Con threshold 0.50: Detecta 42.7% de churns con 66.7% precisión
- Con threshold 0.10: Detecta 100% de churns con 26.3% precisión
- **Decisión:** Usar threshold 0.10 para campañas de bajo costo, 0.50 para campañas premium

### Top 3 Factores Predictivos

1. **Número de quejas/reclamos** (correlación: 0.396)
   - Clientes con churn tienen **3x más quejas** que clientes activos
   
2. **Días sin actividad** (correlación: 0.211)
   - Clientes con churn pasan **57% más días** sin realizar envíos
   
3. **Loss Ratio** (correlación: 0.063)
   - Ratio de siniestralidad superior al 100% indica problemas de rentabilidad

---

## 🛠️ Stack Técnico

### Lenguajes y Librerías
