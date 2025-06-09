# 📊 TFM: Anonimización y Regresión Logística

Este proyecto forma parte del Trabajo de Fin de Máster (TFM) en Big Data e Inteligencia de Negocio.  
Su objetivo es evaluar cómo la anonimización de datos afecta el rendimiento de modelos de clasificación, en particular la regresión logística para detección de fraude financiero.

---

## 📁 Estructura del proyecto
TFM_Anonimizacion_RegresionLogistica/
├── dataset/
│ └── anonimizacion_datos.csv ❌ (no incluido)
├── venv/ ❌ (no incluido)
├── src/
│ └── comparativa_modelos_RL.py
├── notebooks/
│ ├── notebook_EDA_anonimizacion_LLMs.ipynb
│ ├── notebook_analisis_privacidad-utilidad_anonimizacion.ipynb
│ └── notebook_deteccion_fraude_basico.ipynb
├── requirements.txt
├── .gitignore
└── README.md

## ⚠️ Importante: CSV excluido

El archivo `dataset/anonimizacion_datos.csv` fue excluido del repositorio por exceder el límite de 100MB de GitHub.

📥 Puedes descargarlo desde Google Drive:  
🔗 [**Descargar CSV desde Drive**](https://drive.google.com/tu_enlace_aqui)

> Asegúrate de reemplazar el enlace con el tuyo real

---

## ▶️ Cómo ejecutar

```bash
# Activar entorno virtual (Windows)
.\venv\Scripts\activate

# Instalar las dependencias
pip install -r requirements.txt

# Ejecutar el modelo principal
python src/comparativa_modelos_RL.py
