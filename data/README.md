# Datos del Proyecto

## Descripción

Este proyecto utiliza datos sintéticos de seguros de carga.

## Datasets

### seguros_historico.csv (1,500 registros)
- **Período:** 2020-2024
- **Propósito:** Entrenamiento del modelo
- **Variables:** 35 columnas
- **Target:** `churn` (0 = Activo, 1 = Canceló)

### seguros_activos.csv (400 registros)
- **Período:** 2025 (clientes actuales)
- **Propósito:** Predicción de riesgo
- **Variables:** 33 columnas (sin `churn`)

## Variables Principales

**Demográficas:**
- tipo_cliente, sector_industria, region, ciudad

**Actividad:**
- num_envios_ultimo_mes, dias_sin_actividad, frecuencia_envios

**Financieras:**
- prima_mensual_promedio, loss_ratio, variacion_facturacion_pct

**Servicio:**
- satisfaccion_servicio, num_quejas_reclamos, tiempo_respuesta_promedio_dias

**Engagement:**
- llamadas_comercial_trimestre, emails_abiertos_trimestre, uso_portal_digital

## Nota

⚠️ Los archivos CSV no están incluidos por privacidad. Los datos son sintéticos.
