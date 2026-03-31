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

1. **Web Scraping Multifuente:** Extracción automatizada de datos de *Transfermarkt* (valores de mercado), *FBref* (estadísticas deportivas) y portales inmobiliarios (valor del m²).
2. **Pipeline de Estandarización (ETL):** Implementación de un **Diccionario Maestro de Clubes** para resolver la inconsistencia de nombres entre fuentes, logrando una integridad referencial del 100%.
3. **Modelado Predictivo:** Entrenamiento de un algoritmo de *Random Forest* para identificar los drivers de victoria.
4. **Simulación de Negocio:** Proyección de ingresos incrementales por capacidad de aforo y conversión de masa societaria.

---

## 📊 Hallazgos Clave (Insights)

### 1. Drivers de Victoria: La jerarquía sobre el cemento
El análisis de *Feature Importance* revela que la **Diferencia de Valor de Plantel** y la **Brecha de Ingresos** son los factores con mayor peso predictivo. La capacidad física del estadio, por sí sola, tiene una relevancia secundaria en el resultado deportivo inmediato.

![Importancia de Variables](images/importancia_variables.png)

### 2. Correlación de Variables
El mapa de calor confirma una correlación positiva moderada entre la masa societaria y las victorias locales, reforzando la idea de que un estadio más grande permite una base de socios más amplia, lo que eventualmente se traduce en mayor presupuesto para el plantel.

![Mapa de Correlación](images/mapa_correlacion.png)

---

## ⚙️ Validación Técnica del Modelo

Para asegurar la fiabilidad de las conclusiones, se evaluó el rendimiento del modelo de *Random Forest* mediante una **Matriz de Confusión**. Dado que el fútbol es un deporte estocástico (con un alto componente de azar), el modelo busca identificar tendencias estructurales más que resultados exactos de un solo partido.

![Matriz de Confusión](images/matriz_confusion.png)

---

## 🗺️ Análisis Geoespacial: "Billetera Mata Barrio"

Utilizando librerías GIS, mapeamos el rendimiento de localía frente al valor inmobiliario del entorno. Los datos demuestran que no existe una ventaja deportiva inherente a la ubicación geográfica o la riqueza del barrio; el éxito es un producto de la gestión financiera y la escala de infraestructura.

![Mapa de Estadios](images/mapa_estadios.png)

---

## 💰 El Costo de la Nostalgia (Project Finance)

Mantener un aforo de 54.000 personas genera un **Lucro Cesante anual multimillonario**. Nuestro modelo proyecta que pasar a 100.000 localidades destrabaría:
* **Matchday & Hospitality:** +46.000 tickets por partido y nuevas zonas VIP.
* **Optimización de Cuotas:** Conversión masiva de Socios Adherentes a Activos (basado en valores a marzo 2026 de $19.000 y $38.000 ARS).

---

## 💻 Tecnologías Utilizadas

* **Lenguaje:** `Python 3.x`
* **Ingeniería de Datos:** `Pandas`, `BeautifulSoup`, `NumPy`.
* **Machine Learning:** `Scikit-Learn`.
* **Visualización:** `Matplotlib`, `Seaborn`, `Folium`.
* **BI:** Integración con `Power BI` para dashboards ejecutivos.

---
*Proyecto desarrollado para demostrar competencias en **Data Science**, **Evaluación de Riesgos** y **Análisis Estratégico de Negocios**.*

---
*Proyecto desarrollado para demostrar competencias en **Data Science**, **Evaluación de Riesgos** y **Análisis Estratégico de Negocios**.*
