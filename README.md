
# TFM · Anonimización y Regresión Logística para Detección de Fraude

Este repositorio contiene el desarrollo completo de un Trabajo de Fin de Máster (TFM) centrado en técnicas de anonimización de datos y su impacto en modelos de regresión logística aplicados a la detección de fraude.

---

### 📂 Estructura del Proyecto

```
TFM_Anonimizacion_RegresionLogistica/
│
├── dataset/                         # Carpeta reservada para el dataset local (excluido del repo)
│
├── notebooks/                       # Análisis y visualización en Jupyter
│   ├── notebook_analisis_privacidad-utilidad_anonimizacion.ipynb
│   ├── notebook_deteccion_fraude_basico.ipynb
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

### 👨‍🔬 Autor

**Alexi Mendoza**  
Máster en Big Data & Business Intelligence  
TFM defendido en junio 2025

---

### 📜 Licencia

Este proyecto es de uso académico. Para usos comerciales o reproducción del dataset original, contactar con el autor.