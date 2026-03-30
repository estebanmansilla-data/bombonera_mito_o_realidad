# 🏟️ Análisis Actuarial y Predictivo: El Costo de Oportunidad de la "Mística"

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Wrangling-210458)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-F7931E)
![Folium](https://img.shields.io/badge/Folium-Geospatial-77B829)
![Status](https://img.shields.io/badge/Status-Completado-success)

## 📌 Resumen Ejecutivo
¿Es justificable mantener una infraestructura obsoleta basándose en el mito romántico de la "mística"? Este proyecto aborda una de las discusiones más pasionales del fútbol argentino (el impacto de La Bombonera y la localía de Boca Juniors) aplicando **Ciencia de Datos, Machine Learning y Simulaciones Actuariales**. 

A través del cruce de variables financieras, métricas de redes sociales, capacidad de estadios, valores inmobiliarios y resultados deportivos, el modelo cuantifica el verdadero peso de la localía y calcula el costo de oportunidad multimillonario frente a su principal competidor (River Plate).

## 🎯 Objetivos del Proyecto
* **Desmitificar la Localía:** Evaluar mediante modelos predictivos si la presión del estadio y la ubicación geográfica tienen un peso estadístico real sobre el *Win Rate*, o si el éxito obedece a factores financieros.
* **Benchmarking Competitivo:** Medir la brecha de escala en infraestructura y valor de plantel entre Boca Juniors y River Plate.
* **Simulación de Negocio:** Proyectar el impacto deportivo y económico de una hipotética ampliación del estadio a 100,000 espectadores.

## 🗄️ Fuentes de Datos
El pipeline de datos consolida información de múltiples fuentes mediante Web Scraping y APIs:
* **Deportivas:** FBref (Resultados históricos y xG), AFA (Informes de Clubes).
* **Financieras y Mercado:** Transfermarkt (Valor de plantillas, asistencia histórica).
* **Sociales:** Índices de popularidad, encuestas de consultoras y engagement en redes sociales (IPI).
* **Geoespaciales e Inmobiliarias:** MercadoLibre Inmuebles (Valor del m² en USD de los barrios de cada estadio).

## ⚙️ Arquitectura y Metodología
El proyecto se divide en 3 módulos principales iterativos:

1. **Ingeniería de Datos (Web Scraping & ETL):** Construcción de un pipeline de extracción de datos propios desde cero. Se utilizó `requests` y `BeautifulSoup` para raspar (scrape) sistemáticamente datos de resultados históricos (FBref), métricas financieras y de asistencia (Transfermarkt) y valores inmobiliarios por m² (MercadoLibre). Esto incluyó la limpieza, el manejo de excepciones (anti-bloqueos) y la estandarización de diccionarios para consolidar fuentes heterogéneas en una base de datos relacional limpia.
2. **Feature Engineering & Geo-Analysis:** Creación del *Índice de Popularidad Integral (IPI)* y variables maestras relativas (Diferencia de Ingresos, Diferencia de Valor de Plantel). Clusterización geográfica mediante mapas de calor interactivos (`Folium`).
3. **Modelado y Simulación (Montecarlo):** * **Random Forest Classifier:** Para determinar el peso de cada variable financiera/social en la probabilidad de victoria local.
   * **Random Forest Regressor:** Para modelar la curva de ingresos *Matchday*.
   * **Simulación Estocástica:** Escenarios Montecarlo (10,000 iteraciones) aplicando shocks económicos y ruido estocástico para proyectar el rendimiento deportivo bajo nuevas condiciones de infraestructura.

## 📊 Conclusiones Clave y Business Insights

* **1. El Precio Real de la "Mística" (Costo de Oportunidad Financiero)**
El análisis de benchmarking demostró que la ventaja competitiva histórica de la infraestructura actual ha sido neutralizada por la brecha de escala. Al compararse con el estadio de su principal competidor (85k vs. 54k espectadores), mantener el estadio actual bajo el paradigma de la "mística" genera un lucro cesante multimillonario anual. La mística no justifica el costo de oportunidad; lo agrava al limitar severamente la monetización de servicios *Premium/Hospitality*.

* **2. "Billetera Mata Barrio" (Análisis Geoespacial)**
El cruce espacial con el valor del m² (USD) comprobó que la ubicación geográfica no determina el éxito. Los mapas probaron que el *Win Rate* de los clubes está directamente correlacionado con el valor de su plantilla y sus ingresos consolidados, operen en zonas de alto valor inmobiliario (Top CABA) o en zonas populares. El capital financiero dicta la fortaleza de la localía, no el código postal.

* **3. El Efecto Cascada de la Expansión (Simulación Actuarial)**
Las proyecciones confirmaron que el fútbol moderno es un ecosistema de rendimientos escalables. Ampliar la capacidad licúa el déficit de ingresos y genera un "shock económico" que, reinyectado eficientemente en el valor del plantel, aumenta la probabilidad base de victoria. La simulación Montecarlo demuestra un salto estadísticamente significativo en la expectativa de captura de puntos.

## 💻 Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Ingeniería de Datos:** `requests`, `BeautifulSoup` (Web Scraping)
* **Data Wrangling & Análisis:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (Random Forest, MinMaxScaler, Matriz de Confusión)
* **Visualización:** `matplotlib`, `seaborn`, `folium` (Geospatial)

## 🚀 Cómo reproducir este proyecto
1. Clonar el repositorio: `git clone https://github.com/tu_usuario/tu_repositorio.git`
2. Instalar las dependencias: `pip install -r requirements.txt`
3. Ejecutar los notebooks en orden secuencial:
   * `1_Scraping_y_ETL.ipynb`
   * `2_Estandarizacion.ipynb`
   * `3_EDA_y_Modelado.ipynb`

---
*Desarrollado por [Esteban Mansilla / estebanm-mansilla] - Orientado a la toma de decisiones data-driven en la industria deportiva y financiera.*
