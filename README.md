# 🏟️ La Bombonera: ¿Mito o Realidad? 
**Análisis de Costo de Oportunidad, Riesgo Deportivo y Project Finance en el Fútbol Argentino**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

## 📌 Resumen Ejecutivo (Business Case)

El debate histórico del fútbol argentino sostiene que la "mística" de La Bombonera hace ganar partidos a Boca Juniors. Sin embargo, frente a las recientes expansiones de infraestructura de sus principales competidores (e.g., River Plate, con +85.000 localidades), surge una hipótesis financiera: **¿Es la capacidad limitada del estadio (54.000) un ancla económica que impide conformar planteles de mayor jerarquía?**

Este proyecto aplica técnicas de **Ciencia de Datos, Machine Learning y Simulaciones Actuariales (Monte Carlo)** para cuantificar el Costo de Oportunidad (*Lucro Cesante*) de no ampliar el estadio a 100.000 espectadores. La conclusión empírica demuestra que en el deporte moderno, la ventaja competitiva no radica en el código postal ni en la acústica, sino en la capacidad de generar flujo de caja recurrente (*Matchday* y Cuotas Sociales).

---

## 🛠️ Metodología y Arquitectura Analítica

El proyecto se estructuró en fases incrementales, destacando un robusto proceso de ingeniería de datos previo al modelado:

1. **Web Scraping Multifunte:** Extracción automatizada de datos de *Transfermarkt* (valores de mercado), *FBref* (estadísticas deportivas) y portales inmobiliarios (valor del m²), utilizando `BeautifulSoup` y `Requests`.
2. **Pipeline de Estandarización (ETL):** Implementación de un **Diccionario Maestro de Clubes** para resolver la inconsistencia de nombres entre fuentes (e.g., "Boca", "C.A.B.J.", "Boca Juniors"), logrando una integridad referencial del 100% en el *merge* final.
3. **Modelado Predictivo (Random Forest):** Evaluación del peso de variables macroeconómicas y de infraestructura sobre el resultado deportivo.
4. **Simulación Estocástica (Monte Carlo):** Proyección de ingresos a largo plazo para mitigar la varianza inherente al fútbol.

---

## 📊 Hallazgos Clave (Insights)

### 1. ¿Qué determina realmente la victoria?
A través del análisis de *Feature Importance*, observamos que la **jerarquía del plantel** y los **ingresos operativos** tienen un peso superior a cualquier factor ambiental.

![Importancia de Variables](Visualizaciones/importancia_variables.png)

### 2. El Fútbol es Estocástico
El modelo de clasificación arrojó un *Accuracy* del 51% para predecir victorias locales. Este resultado, lejos de ser una falla, documenta la naturaleza estocástica del deporte: a corto plazo, un partido es ruido estadístico; a largo plazo (27 fechas), la billetera y la estructura dominan la tendencia.

![Matriz de Correlación](Visualizaciones/matriz_correlacion.png)

### 3. El Costo de la Nostalgia (Project Finance)
Mantener un aforo de 54.000 personas genera un **Lucro Cesante anual multimillonario**. Nuestro modelo proyecta que pasar a 100.000 localidades destrabaría:
* **Matchday & Hospitality:** +46.000 tickets por partido y nuevas zonas VIP cotizadas en moneda dura.
* **Demanda Latente (Socios):** Optimización del embudo de conversión de Socios Adherentes a Activos (basado en cuotas reales a marzo 2026 de $19.000 y $38.000 ARS).

---

## 🗺️ Análisis Geoespacial: "Billetera Mata Barrio"
Utilizando `Folium`, se mapeó la relación entre el rendimiento local y el entorno socioeconómico de los estadios. Se concluye que no existe relación causal entre la riqueza del barrio y el *Win Rate*.

![Mapa de Estadios](Visualizaciones/mapa_estadios.png)

---

## ⚠️ Notas Metodológicas (Data Caveats)

> **Sesgo de Selección Inmobiliaria:** El valor del m² extraído mediante scraping sobreestima el valor en zonas de alta disparidad socioeconómica (e.g., Florencio Varela o Sarandí) al no registrar viviendas informales. Para entornos productivos, se recomienda cruzar con indicadores NBI del INDEC.

---

## 💻 Tecnologías Utilizadas

* **Lenguaje:** `Python 3.x`
* **Ingeniería de Datos:** `Pandas`, `BeautifulSoup` (Scraping), `NumPy`.
* **Machine Learning:** `Scikit-Learn` (Random Forest).
* **Visualización:** `Matplotlib`, `Seaborn`, `Folium` (GIS).
* **BI:** Integración con `Power BI` para despliegue de *Dashboards* ejecutivos.

---
*Proyecto desarrollado para demostrar competencias en **Data Science**, **Evaluación de Riesgos** y **Análisis Estratégico de Negocios**.*
