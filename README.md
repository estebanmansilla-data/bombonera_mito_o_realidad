# 🏟️ La Bombonera: ¿Mito o Realidad? 
**Análisis de Costo de Oportunidad, Riesgo Deportivo y Project Finance en el Fútbol Argentino**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Folium](https://img.shields.io/badge/Folium-77B829?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

## 📌 Resumen Ejecutivo (Business Case)

El debate histórico del fútbol argentino sostiene que la "mística" de La Bombonera hace ganar partidos a Boca Juniors. Sin embargo, frente a las recientes expansiones de infraestructura de sus principales competidores (ej. River Plate, con +85.000 localidades), surge una hipótesis financiera: **¿Es la capacidad limitada del estadio (54.000) un ancla económica que impide conformar planteles de mayor jerarquía?**

Este proyecto aplica técnicas de **Ciencia de Datos, Machine Learning y Simulaciones Actuariales (Montecarlo)** para cuantificar el Costo de Oportunidad (Lucro Cesante) de no ampliar el estadio a 100.000 espectadores. La conclusión empírica demuestra que en el deporte moderno, la ventaja competitiva no radica en el código postal ni en la acústica, sino en la capacidad de generar flujo de caja recurrente (*Matchday* y Cuotas Sociales).

---

## 🛠️ Metodología y Arquitectura Analítica

El proyecto se estructuró en fases incrementales de complejidad analítica, pasando de la estadística descriptiva a la proyección financiera:

1. **Extracción y Limpieza (EDA):** Procesamiento de datasets históricos de resultados deportivos e indicadores financieros.
2. **Modelado Predictivo (Random Forest):** Evaluación del peso de las variables macroeconómicas sobre el resultado deportivo.
3. **Análisis Geoespacial (Folium):** Mapeo del rendimiento local vs. valor inmobiliario del entorno (USD/m²).
4. **Simulación Estocástica (Montecarlo):** Proyección a largo plazo para mitigar la varianza estadística del fútbol.
5. **Modelado Financiero:** Estimación de ingresos incrementales mediante *Waterfall Charts* y embudos de conversión societaria.

---

## 📊 Hallazgos Clave (Insights)

### 1. El Fútbol es Estocástico: La billetera domina a largo plazo
El modelo de clasificación *Random Forest* arrojó un *Accuracy* del 51% para predecir victorias locales. Lejos de ser un modelo deficiente, este resultado documenta la naturaleza estocástica del deporte a corto plazo: **un partido aislado es ruido estadístico**. Sin embargo, el análisis de *Feature Importance* y las proyecciones de Montecarlo demuestran que, a lo largo de una temporada de 27 fechas, la **Diferencia de Valor de Plantel** se impone de forma abrumadora sobre el factor "estadio".

### 2. "Billetera Mata Barrio": Desmitificando la Localía
El análisis geoespacial y de correlación visualiza que no existe relación causal entre la riqueza del barrio donde se ubica el estadio y el *Win Rate* del equipo local. Clubes con gestiones financieras eficientes en zonas periféricas logran tasas de victoria superiores a clubes ubicados en los corredores inmobiliarios más caros de Buenos Aires. 

### 3. El Costo de la Nostalgia (Project Finance)
Mantener un aforo de 54.000 personas genera un **Lucro Cesante anual multimillonario**. Nuestro modelo proyecta que pasar a un estadio de 100.000 localidades destrabaría:
* **Matchday & Hospitality:** +46.000 tickets por partido y nuevas zonas VIP cotizadas en moneda dura.
* **Demanda Latente (Socios):** Una inyección financiera drástica al destrabar el embudo de Socios Adherentes a Activos (calculado con cuotas reales a marzo 2026 de $19.000 y $38.000 ARS, respectivamente).

Este flujo de caja incremental es de tal magnitud que justifica ampliamente la estructuración de un crédito internacional para la construcción de una nueva arena acústica de vanguardia.

---

## ⚠️ Notas Metodológicas y Sesgos de Datos (Data Caveats)

Como parte de las buenas prácticas en Ingeniería de Datos, es imperativo documentar las limitaciones de las fuentes utilizadas:

> **Sesgo de Selección Inmobiliaria (*Selection Bias*):**
> La variable del valor del m² (USD) extraída mediante *Web Scraping* de portales de mercado formal presenta limitaciones de representatividad en zonas de alta disparidad socioeconómica. Por ejemplo, el indicador sobreestima el valor del entorno de clubes como Defensa y Justicia (Florencio Varela) al no registrar en internet las viviendas informales adyacentes al estadio. Esto genera una anomalía estadística al compararlo con zonas de urbanización más homogénea y consolidada como Avellaneda. Para entornos productivos, se recomienda cruzar esta información con variables censales estructurales (ej. NBI del INDEC).

---

## 💻 Tecnologías Utilizadas

* **Lenguaje:** `Python 3.x`
* **Manipulación de Datos:** `Pandas`, `NumPy`
* **Machine Learning:** `Scikit-Learn` (Random Forest, Classification Reports)
* **Visualización Dinámica y Estática:** `Matplotlib`, `Seaborn`, `Folium` (Mapas GIS)
* **Business Intelligence:** Integración planificada con `Power BI` para despliegue de *Dashboards* ejecutivos.

---

*Proyecto desarrollado para demostrar competencias en **Data Science**, **Evaluación de Riesgos** y **Análisis Estratégico de Negocios**.*
