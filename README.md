# 📊 Predicción de Churn - Desafío Telecom X (Parte 2)

Este repositorio contiene la solución completa a la segunda parte del **Desafío Telecom X** propuesto por Alura. El objetivo principal de este proyecto es asumir el rol de Científico de Datos para construir, evaluar y analizar modelos predictivos de Machine Learning que permitan anticipar la cancelación de servicios (Churn) por parte de los clientes de una empresa de telecomunicaciones.

## 🎯 Objetivos del Proyecto
* **Procesamiento de Datos:** Extraer, limpiar y transformar un dataset estructurado en formato JSON.
* **Análisis Exploratorio (EDA):** Identificar correlaciones clave entre los atributos del cliente y el abandono del servicio.
* **Modelado Predictivo:** Entrenar y comparar cuatro algoritmos de clasificación para manejar datos desbalanceados.
* **Interpretabilidad:** Extraer las variables más críticas (Feature Importance) que impulsan la decisión de cancelar.
* **Estrategia de Negocio:** Proponer recomendaciones accionables basadas en datos empíricos para mejorar la retención de clientes.

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3
* **Manipulación y Análisis de Datos:** `pandas`, `numpy`, `json`
* **Visualización:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (Regresión Logística, K-Nearest Neighbors, Random Forest, Support Vector Machines)

## 📂 Estructura del Repositorio
* `TelecomX_LATAM.ipynb`: Jupyter Notebook principal que contiene todo el código ejecutado paso a paso (Extracción, Transformación, Entrenamiento, Evaluación e Importancia de Variables).
* `TelecomX_Data.json`: Archivo de datos original (Raw Data) que contiene la información de los clientes, servicios y facturación.
* `TelecomX_diccionario.md`: Diccionario de datos que detalla el significado de cada columna/variable del dataset.

## ⚙️ Instrucciones de Uso y Ejecución

Para ejecutar o revisar este proyecto en tu entorno local o en la nube (como Google Colab), sigue estos pasos:

1.  **Instala las dependencias necesarias:**
    Asegúrate de tener instaladas las librerías requeridas ejecutando el siguiente comando en tu terminal o celda de código:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```

2.  **Configuración del Entorno:**
    Descarga los archivos de este repositorio y asegúrate de que el archivo `TelecomX_Data.json` se encuentre en la misma carpeta o directorio raíz que el notebook `TelecomX_LATAM.ipynb`.

3.  **Ejecución del Notebook:**
    Abre el notebook y ejecuta las celdas secuencialmente:
    * **Sección 1 y 2:** Carga del JSON, aplanamiento, limpieza de valores nulos (NaN) y codificación de variables categóricas (One-Hot Encoding).
    * **Sección 3:** Entrenamiento de los 4 modelos predictivos y generación de visualizaciones (Matrices de Confusión y Curva ROC comparativa).
    * **Sección 4:** Extracción y graficación de la importancia de las variables (Feature Importance y Análisis de Coeficientes).

## 📈 Hallazgos y Resultados Clave
Tras evaluar los modelos (donde la Regresión Logística y SVM destacaron por su capacidad para distinguir la frontera de decisión), se identificaron los siguientes detonantes principales de abandono:

1.  **El Tipo de Contrato (Month-to-month):** Es el factor de riesgo número uno. Los clientes que pagan mes a mes carecen de barreras de salida y abandonan con facilidad.
2.  **El Cargo Total y Mensual:** Existe una altísima sensibilidad al precio. Facturas elevadas aumentan drásticamente la probabilidad de fuga.
3.  **Servicio de Internet de Fibra Óptica:** A pesar de ser un servicio premium, está fuertemente correlacionado con el abandono, lo que sugiere problemas de calidad, soporte o percepción de valor frente al precio.

## 💡 Recomendaciones Estratégicas
* **Incentivos de Migración:** Crear campañas para trasladar a los clientes de contratos mensuales a planes anuales, ofreciendo beneficios exclusivos (ej. un mes gratis o mejoras de velocidad).
* **Auditoría Técnica:** Investigar la infraestructura y el soporte del servicio de Fibra Óptica para solucionar las causas subyacentes de la insatisfacción.
* **Retención Proactiva:** Utilizar el modelo predictivo para identificar clientes en alto riesgo (especialmente aquellos con contratos mensuales y facturas altas) y ofrecerles bonos de fidelización automáticos.

---
**Desarrollado por [Tu Nombre/Usuario]** para el Desafío Alura.
