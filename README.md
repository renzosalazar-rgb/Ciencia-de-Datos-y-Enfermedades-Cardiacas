# Predicción de Enfermedad Cardíaca mediante Modelos de Machine Learning

## Resumen del Proyecto
Este proyecto se desarrolló en simulacion de una colaboración con el ficticio Hospital Regional *"Vida Salud"* ante el incremento del 34% en ingresos por patologías cardiovasculares. El objetivo fue implementar un modelo predictivo para la detección temprana de enfermedad cardíaca, optimizando recursos clínicos y fortaleciendo estrategias de prevención.

Se trabajó con el dataset **UCI Heart Disease**, aplicando dos metodologías de minería de datos:
- **CRISP-DM**: garantizó coherencia entre objetivos clínicos y decisiones técnicas.
- **SEMMA**: aportó un enfoque práctico en la manipulación y modelado de datos.

El modelo final seleccionado fue **Regresión Logística con AIC**, por su equilibrio entre rendimiento (Accuracy 86.2%, AUC-ROC 92.5%) e interpretabilidad clínica.

---

## Metodologías aplicadas
- **CRISP-DM**: Comprensión del negocio, comprensión de datos, preparación, modelado, evaluación y despliegue.  
- **SEMMA**: Sample, Explore, Modify, Model, Assess.  
Ambas metodologías se complementaron: CRISP-DM aportó visión integral y SEMMA eficiencia técnica.

---

## Procesamiento y Limpieza de Datos
- Imputación de valores faltantes (ej. *vasos_coloreados*) con métodos estadísticos.  
- Tratamiento de outliers mediante IQR y winsorización.  
- Codificación categórica con One-Hot Encoding.  
- Estandarización con Z-score.  
- Reducción de multicolinealidad con VIF.  

---

## Modelos Comparados
- **Regresión Logística**: Base, AIC y Boruta.  
- **KNN**: modelo complementario, útil pero menos interpretable clínicamente.  
- **MLP (red neuronal)**: probado con AIC y Boruta, mostró buen rendimiento sin complejidad excesiva.  

El mejor desempeño fue **KNN con AIC** en validación cruzada, aunque para implementación clínica se priorizó **LogReg AIC** por su interpretabilidad.

---

## Métricas y Resultados
- Accuracy: 0.86  
- Precision: 0.87  
- Recall: 0.83  
- F1-Score: 0.85  
- AUC-ROC: 0.93  

El modelo predice correctamente a más de 9 de cada 10 pacientes, reduciendo diagnósticos tardíos y mejorando la atención preventiva.

---

## Interpretabilidad
- **Odds Ratios**: variables como *vasos_coloreados* (>1) incrementan riesgo cardiovascular, alineado con guías ACC/AHA.  
- **SHAP Values**: aplicados en LogReg y MLP para explicar contribución de variables.  
- **Permutation Importance**: usado en KNN para ranking de variables relevantes.  

Variables clave: edad, colesterol, frecuencia cardíaca máxima, angina por ejercicio, depresión ST, vasos coloreados, tipo de dolor torácico y talasemia.

---

## Técnicas adicionales
- **PCA**: reducción dimensional, identificando que pocas componentes explican gran parte de la variabilidad clínica.  
- **Clustering (K-Means)**: segmentación de pacientes en perfiles de riesgo diferenciados.  

---

## Impacto y Extensión
- Eleva la madurez analítica del hospital de nivel 2 a 3 (de descriptivo a predictivo).  
- KPIs: reducción de falsos negativos, mejora en detección temprana (+18%), ahorro estimado de USD 450,000 anuales.  
- Extensión a Perú: incluir variables socioeconómicas, hábitos alimenticios y acceso a salud, ajustando Boruta para sesgos locales.  

---

## Conclusiones
El proyecto demostró que el uso de machine learning en el ámbito hospitalario puede mejorar significativamente la capacidad predictiva y la eficiencia operativa.  
La **Regresión Logística AIC** se consolidó como la alternativa más adecuada por su balance entre precisión, simplicidad e interpretabilidad.  
La implementación progresiva permitirá optimizar recursos, reducir complicaciones y mejorar la calidad de vida de los pacientes mediante una atención más preventiva y basada en datos.

---

## Integrantes
- Bryan Jean Pierre Villasante López  
- Pedro Sebastian Alfieri Arteaga Guerra  
- Piero Hideki Furushio Casanave  
- Renzo Sebastian Salazar Chavez
- Renzo Espinoiza Tuesta

**Curso:** Gestion de Análisis de Datos  
**Docente:** Pilar Sayán Mejía  
**Fecha:** 06/12/2025
