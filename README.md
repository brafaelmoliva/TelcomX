# 📊 Telecom X - Análisis de Churn (Evasión de Clientes)

![Estatus del Proyecto](https://img.shields.io/badge/STATUS-EN%20DESARROLLO-green)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Pandas](https://img.shields.io/badge/Library-Pandas-orange)

Este proyecto forma parte del desafío de **Telecom X**, donde actúo como analista de datos para identificar los factores que influyen en la pérdida de clientes (Churn). El objetivo es realizar un proceso de **ETL** y un **Análisis Exploratorio (EDA)** para entregar datos limpios e insights estratégicos al equipo de Data Science.

## 📁 Estructura del Proyecto

* `Desafio_TelecomX_Churn.ipynb`: Notebook de Google Colab con todo el código de extracción, limpieza y visualización.
* `TelecomX_Data.json`: Fuente de datos original (vía API).
* `README.md`: Documentación del proyecto.

## 🛠️ Tecnologías Utilizadas

* **Python 3**
* **Pandas**: Manipulación y limpieza de datos.
* **Requests**: Extracción de datos desde API.
* **Matplotlib & Seaborn**: Visualizaciones estratégicas.
* **Google Colab**: Entorno de desarrollo.

## 🚀 Proceso de Desarrollo (ETL)

### 1. Extracción (Extract)
Se importaron los datos en formato JSON desde la API oficial de Telecom X. Debido a la estructura anidada del archivo, se aplicó una normalización para convertir los diccionarios internos (`customer`, `phone`, `internet`, `account`) en un DataFrame plano.

### 2. Transformación (Transform)
* **Limpieza de nombres:** Se eliminaron los prefijos de las columnas para mejorar la legibilidad.
* **Tratamiento de tipos:** La columna `Total` se convirtió de texto a numérico (`float`), gestionando valores nulos para clientes con 0 meses de antigüedad.
* **Calidad de datos:** Se verificaron y eliminaron registros duplicados e inconsistencias en las categorías.

### 3. Carga y Análisis (Load & Analysis)
Se realizaron visualizaciones para identificar patrones de fuga:
* Análisis de Churn por tipo de contrato.
* Relación entre cargos mensuales y evasión.
* Impacto de la antigüedad (`tenure`) en la retención.

## 📈 Hallazgos Principales (Insights)

1.  **Contratos Críticos:** Los clientes con contrato **mes a mes** tienen la tasa de abandono más alta.
2.  **Periodo de Riesgo:** La mayoría de las cancelaciones ocurren en los primeros **12 meses**.
3.  **Métodos de Pago:** Existe una correlación alta de evasión en clientes que utilizan **Electronic Check**.

## 🔧 Cómo ejecutar el proyecto

1. Clona este repositorio.
2. Sube el archivo `.ipynb` a [Google Colab](https://colab.research.google.com/).
3. Ejecuta las celdas en orden. No es necesario descargar los datos manualmente, ya que el script los consume directamente de la API.

---
**Desarrollado por:** Brian Mendoza
*Proyecto realizado para el programa One - Alura Latam*
