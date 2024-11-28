# 📈 Optimización de Portafolios de Inversión con IA

Este repositorio contiene la implementación de un proyecto de optimización de portafolios de acciones, combinando **Redes Neuronales LSTM** y **Procesamiento de Lenguaje Natural (PLN)** para realizar predicciones financieras. El proyecto integra datos históricos, análisis de sentimientos y aprendizaje profundo para construir y optimizar un portafolio de inversión.

## 📋 Tabla de Contenidos
1. [Resumen del Proyecto](#resumen-del-proyecto)
2. [Características](#características)
3. [Conjunto de Datos](#conjunto-de-datos)
4. [Metodología](#metodología)
5. [Resultados](#resultados)
6. [Requisitos](#requisitos)
7. [Cómo Ejecutar](#cómo-ejecutar)

---

## 🔍 Resumen del Proyecto
El objetivo de este proyecto es predecir precios de acciones utilizando modelos LSTM que integran datos financieros históricos y análisis de sentimientos extraídos de noticias financieras y publicaciones en Reddit. Estas predicciones se emplean para construir un portafolio optimizado utilizando teoría moderna de portafolios, maximizando el **Ratio de Sharpe**.

---

## ✨ Características
- 📊 **Análisis de Datos Históricos:** Integración de precios de cierre y indicadores técnicos (e.g., medias móviles).
- 🧠 **Modelos LSTM:** Diseñados para modelar dependencias temporales en series de tiempo financieras.
- 📰 **Análisis de Sentimientos:** Datos extraídos mediante:
  - **VADER:** Para publicaciones en Reddit.
  - **FinBERT:** Para noticias financieras.
- 🛠 **Optimización de Portafolios:** Maximiza los rendimientos ajustados al riesgo utilizando el Ratio de Sharpe.
- 📈 **Comparación:** Comparación del rendimiento del portafolio con los índices **XLK** y **S&P 500**.

---

## 📂 Conjunto de Datos
### Fuentes:
1. **API de Yahoo Finance:** Precios históricos de las acciones seleccionadas del índice XLK.
2. **API de Reddit:** Sentimientos financieros extraídos del subreddit `r/WallStreetBets`.
3. **Noticias de Yahoo Finance:** Titulares y artículos para análisis de sentimientos con FinBERT.

### Preprocesamiento:
- Normalización de datos financieros utilizando **MinMaxScaler**.
- Cálculo de medias móviles (10, 30 y 60 días) para el análisis de tendencias.
- Extracción diaria de puntajes de sentimiento para noticias financieras y publicaciones en Reddit.

---

## ⚙️ Metodología
1. **Recolección de Datos:**
   - Obtención de precios históricos y titulares de noticias.
   - Extracción de datos de sentimiento de Reddit y Yahoo Finance.
2. **Preprocesamiento:**
   - Normalización de datos financieros.
   - Procesamiento de texto para análisis de sentimientos.
3. **Modelado:**
   - Entrenamiento de modelos LSTM con características que incluyen indicadores financieros y puntajes de sentimiento.
   - Evaluación de los modelos utilizando métricas como **MSE**, **MAE** y **R²**.
4. **Construcción del Portafolio:**
   - Selección de acciones con rendimientos esperados positivos.
   - Optimización de pesos del portafolio utilizando teoría moderna de portafolios.
5. **Benchmarking:**
   - Comparación del rendimiento del portafolio con los índices **XLK** y **S&P 500**.

---

## 📊 Resultados
- **Rendimiento del Modelo:** La incorporación del análisis de sentimientos mejoró la precisión de las predicciones en comparación con modelos que utilizan únicamente datos históricos.
- **Optimización del Portafolio:** El portafolio optimizado superó a los índices XLK y S&P 500 en términos de Ratio de Sharpe y rendimientos acumulados durante el período de evaluación.
- Los resultados detallados y visualizaciones se encuentran en el informe del proyecto.

---

## 🖥 Requisitos
Para replicar los experimentos, asegúrate de tener instalados los siguientes componentes:
- Python 3.9+
- Bibliotecas clave: `numpy`, `pandas`, `matplotlib`, `torch`, `pytorch-lightning`, `yfinance`, `transformers`, `asyncpraw`, `nltk`, `scikit-learn`.

---

## 🚀 Cómo Ejecutar
1. **Abrir la notebook en Google Colab:**
   - Accede a la notebook haciendo clic en el siguiente enlace: [Notebook en Google Colab](URL_DE_LA_NOTEBOOK).

2. **Configurar el entorno:**
   - Asegúrate de que tu entorno de ejecución esté configurado para usar una GPU:
     1. Ve a `Entorno de ejecución` en el menú superior.
     2. Selecciona `Cambiar tipo de entorno de ejecución`.
     3. En `Acelerador de hardware`, selecciona `GPU`.

3. **Ejecutar la notebook:**
   - Sigue las instrucciones en la notebook. Cada celda está organizada para ejecutarse secuencialmente:
     1. Carga las bibliotecas y configura las dependencias.
     2. Descarga los datos financieros y de noticias.
     3. Entrena los modelos y construye el portafolio optimizado.
     4. Analiza las métricas y visualizaciones generadas.

4. **Exportar resultados:**
   - Los resultados generados, como visualizaciones y archivos `.csv`, se almacenarán directamente en el entorno temporal de Google Colab. Puedes descargarlos a tu máquina local utilizando la opción `Archivos` en la barra lateral de Colab.

5. **Guardar cambios:**
   - Si realizas modificaciones, guarda una copia de la notebook en tu Google Drive o en tu repositorio de GitHub.

[Open In Colab](https://colab.research.google.com/drive/1vT70eSgPK2_vKaUR1k2bAAgP7fEzjs4R?usp=sharing)
