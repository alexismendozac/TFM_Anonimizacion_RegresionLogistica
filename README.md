
# TFM · Anonimización y Regresión Logística para Detección de Fraude

Este repositorio contiene el desarrollo completo de un Trabajo de Fin de Máster (TFM) centrado en técnicas de anonimización de datos y su impacto en modelos de regresión logística aplicados a la detección de fraude.

---


### 📄 Documento del Trabajo Final de Máster

El informe completo del TFM está disponible en el siguiente enlace:

📎 [TFM - Anonimización y Cumplimiento del GDPR con Modelos LLM](https://drive.google.com/drive/folders/1bU1SSvt7IW3EzleY2cjp6QdY42P9pYrP)

Incluye fundamentos legales, técnicas avanzadas de protección de datos (k-anonimato, l-diversidad, privacidad diferencial) y evaluación empírica con modelos de clasificación (Random Forest, XGBoost, Regresión Logística).


---

### 📂 Estructura del Proyecto

```
TFM_Anonimizacion_RegresionLogistica/
│
├── dataset/                         # Carpeta reservada para el dataset local (excluido del repo)
│
├── notebooks/                       # Análisis y visualización en Jupyter
│   ├── notebook_analisis_privacidad-utilidad_anonimizacion.ipynb
│   ├── notebook_deteccion_fraude_basico.ipynbgit add .git add .
│   └── notebook_EDA_anonimizacion_LLMs.ipynb
│
├── src/                             # Scripts de análisis y modelos
│   ├── comparativa_modelos_RL.py
│   ├── eda_anonimizacion_fraud_detection.py
│   └── eda_anonimizacion_modular.py
│
├── venv/                            # Entorno virtual (ignorado por Git)
│
├── requirements.txt                # Librerías necesarias
├── .gitignore                      # Archivos ignorados (venv, dataset, logs, etc.)
├── .gitattributes
└── README.md                       # Este archivo
```

---

### 📁 Dataset

🔐 **Por motivos de privacidad, el dataset no se encuentra en este repositorio.**  
Puedes descargarlo desde el siguiente enlace de Google Drive:

📎 [`anonimizacion_datos.csv`](https://drive.google.com/drive/u/0/folders/15hNc2cTtTDilX9EkOmLgEerf5v53ZScB)

Una vez descargado, colócalo en la siguiente ruta local:

```
dataset/anonimizacion_datos.csv
```

> ✅ Este archivo está incluido en `.gitignore` para evitar su exposición pública.

---

### 📊 Contenido de los notebooks

- `notebook_EDA_anonimizacion_LLMs.ipynb`  
  Exploración de datos y visualización con soporte de LLMs para comprensión semántica de variables.

- `notebook_deteccion_fraude_basico.ipynb`  
  Modelo base de regresión logística sobre datos sin anonimizar.

- `notebook_analisis_privacidad-utilidad_anonimizacion.ipynb`  
  Análisis de cómo la anonimización afecta la precisión del modelo, con métricas de privacidad y utilidad.

---

### 🧠 Scripts principales (`/src`)

- `eda_anonimizacion_modular.py`  
  Exploración de datos modularizada y reutilizable para múltiples escenarios de anonimización.

- `eda_anonimizacion_fraud_detection.py`  
  Preprocesamiento de variables y generación de features relevantes para detección de fraude.

- `comparativa_modelos_RL.py`  
  Comparación entre modelos entrenados con datos originales vs. anonimizados.
---

## 🧠 Arquitectura de la Solución – Regresión Logística

### 🔁 Pipeline de Procesamiento

```mermaid
graph TD
    A[📁 Dataset PaySim1] --> B[🛡️ Seudonimización (SHA-256)]
    B --> C[🔒 K-Anonimato (k=10)]
    C --> D[🎯 L-Diversidad (l=2)]
    D --> E[🧪 Evaluación de privacidad (ε=2.0)]
    E --> F[📊 Preprocesamiento RL]
    F --> G[📉 Entrenamiento RL]
    G --> H[📜 Evaluación GDPR]
    H --> I[🎓 Visualización e Interpretación]

    Preprocesamiento RL: OneHotEncoding, normalización, eliminación de outliers, split 80/20.

    Entrenamiento RL: Scikit-learn / statsmodels, penalización, AUC, matriz de confusión.

    Evaluación GDPR: simulación de reidentificación y análisis post-anonimización.
---
### 📈 Resultados Principales: Regresión Logística

Comparación entre el modelo entrenado con datos originales vs. datos anonimizados:

| Métrica      | Original | Anonimizado | Impacto  | Interpretación            |
|-------------|----------|-------------|----------|---------------------------|
| Precisión   | 99.91%   | 99.91%      | ±0.00%   | ✅ Estabilidad total       |
| Sensibilidad| 39.45%   | 41.68%      | +2.23%   | 🟢 Ligera mejora inesperada |
| F1-Score    | 52.46%   | 54.86%      | +2.40%   | 🟢 Optimización emergente |

**🟢 Fortalezas:**

- *Mejora tras anonimización*: Se observa un efecto de regularización implícita.
- *Interpretabilidad superior*: Modelo simple y explicativo.
- *Cumplimiento normativo*: Buena base para auditorías con GDPR.

**🔴 Limitaciones:**

- *Sensibilidad aún baja*: No es ideal como solución única en detección de fraude.
- *Modelo lineal*: Menor capacidad para patrones complejos comparado con RF o XGBoost.


---
### 🛠️ Instalación y entorno

1. Clona el repositorio:

```bash
git clone https://github.com/tuusuario/TFM_Anonimizacion_RegresionLogistica.git
```

2. Crea el entorno virtual y actívalo:

```bash
python -m venv venv
venv\Scripts\activate    # En Windows
```

3. Instala las dependencias:

```bash
pip install -r requirements.txt
```

---

### 🧪 Reproducibilidad

Asegúrate de colocar el archivo `anonimizacion_datos.csv` en la ruta `dataset/`. Luego puedes correr:

```bash
jupyter notebook
```

Y explorar los notebooks dentro de la carpeta `notebooks/`.

---
### 🌐 Presentación Interactiva

Accede a la presentación de tu Trabajo Final de Máster (TFM) aquí:
🔗 TFM Anonimización y Regresión Logística (Genially)

---

### 👨‍🔬 Autor

**Alexi Mendoza**  
Máster en Big Data & Business Intelligence  
TFM defendido en junio 2025

---

### 📜 Licencia

Este proyecto es de uso académico. Para usos comerciales o reproducción del dataset original, contactar con el autor.