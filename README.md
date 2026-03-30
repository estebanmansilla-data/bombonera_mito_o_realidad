# 🏟️ La Bombonera: ¿Mito o Realidad? Modelando el Costo de Oportunidad de la "Mística"

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Wrangling-210458)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-F7931E)
![Folium](https://img.shields.io/badge/Folium-Geospatial-77B829)

## 📌 El Debate
¿Un estadio puede ganar partidos por sí solo, o aferrarse a una infraestructura de 1940 frena el crecimiento institucional? Este proyecto aborda el histórico debate sobre la "mística" de La Bombonera utilizando **Data Science, Machine Learning y Simulaciones Estocásticas**.

El objetivo es cuantificar si las características intangibles del estadio de Boca Juniors realmente impactan en el rendimiento deportivo, o si la limitación de su capacidad (54,000 espectadores) actúa como un techo financiero. Utilizando a River Plate (estadio de 85,000+ espectadores) como *benchmark* competitivo, este estudio proyecta los ingresos y resultados deportivos potenciales de un estadio para más de 100,000 personas.

## 🎯 Objetivos Analíticos
1. **Desmitificar la Localía:** Determinar, mediante modelos de clasificación, el peso real de las variables de infraestructura frente a las variables financieras en la probabilidad de victoria local.
2. **Gap Analysis (Benchmarking):** Cuantificar la brecha de ingresos *Matchday* y valor de plantel frente al rival directo.
3. **Proyección y Simulación:** Aplicar modelos de regresión y simulaciones de Montecarlo para calcular el lucro cesante actual y predecir el salto en el *Win Rate* bajo un escenario de modernización estructural (estadio mundialista).

## ⚙️ Arquitectura de Datos y Metodología
El proyecto se estructura en tres fases modulares:

1. **Ingeniería de Datos (Scraping & ETL):** Construcción de un pipeline para extraer datos crudos de FBref (xG, resultados), Transfermarkt (asistencia, valor de mercado), informes de AFA y MercadoLibre (valor m² USD). Normalización de diccionarios y consolidación en DataFrames estructurados.
2. **Feature Engineering & Análisis Espacial:** Creación de métricas relativas (diferenciales de ingresos, ratios de ocupación) y desarrollo del *Índice de Popularidad Integral (IPI)*. Modelado geoespacial (`Folium`) para cruzar éxito deportivo con valor inmobiliario.
3. **Machine Learning & Simulación Actuarial:** 
   * Entrenamiento de modelos **Random Forest** (Classifier y Regressor) para identificar *Feature Importance* y proyectar curvas de ingresos.
   * **Simulación Montecarlo (10,000 iteraciones)** aplicando shocks de capital con rendimientos decrecientes y ruido estocástico, para modelar universos paralelos de rendimiento deportivo.

## 📊 Business Insights: Mito vs. Realidad

* **Billetera Mata Barrio (Finanzas > Arquitectura):** El análisis de importancia de variables y el clustering espacial demuestran que el éxito sostenido de la localía se explica por el valor diferencial del plantel y los ingresos consolidados, no por el barrio ni la acústica.
* **El Costo de Oportunidad Multimillonario:** El benchmarking revela que la "mística" no justifica la brecha de escala. Mantener el aforo actual impone un techo de cristal que limita la monetización y ensancha la ventaja financiera del principal competidor.
* **El Efecto Multiplicador (Visión Global):** Las simulaciones predictivas confirman que un estadio de 100,000+ lugares no solo absorbe la demanda histórica insatisfecha de la base de popularidad más grande del país, sino que ese "shock" económico reinvertido mejora la probabilidad base de victoria tanto de local como de visitante.

## 🚀 Estructura del Repositorio
* `1_Scraping_y_ETL.ipynb`: Ingesta automatizada y limpieza inicial.
* `2_Estandarizacion.ipynb`: Unificación de identidades y métricas financieras.
* `3_EDA_y_Modelado.ipynb`: Análisis exploratorio, benchmarking, predicciones y simulaciones.

---
*Análisis desarrollado para traducir pasiones deportivas en decisiones estratégicas fundamentadas en datos.*
