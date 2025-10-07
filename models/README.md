
# Modelos del Proyecto

## Modelo Final

**Algoritmo:** Random Forest Classifier  
**Features:** 40 variables (13 categóricas + 27 numéricas)  
**Performance:**
- ROC-AUC: 0.XXX
- Accuracy: 80.3%
- Recall: 100% (threshold 0.10)

## Archivos Generados

Al ejecutar el notebook se crean:
- `modelo_churn_final.pkl` - Modelo entrenado
- `label_encoders.pkl` - Encoders categóricos
- `scaler.pkl` - Escalador de variables
- `features.pkl` - Lista de features
- `threshold_config.pkl` - Config de thresholds

⚠️ Los archivos .pkl no están en el repo por tamaño. Se regeneran ejecutando el notebook.

## Modelos Comparados

1. **Random Forest** ⭐ (seleccionado)
2. Gradient Boosting
3. Logistic Regression
4. Decision Tree
5. Naive Bayes
