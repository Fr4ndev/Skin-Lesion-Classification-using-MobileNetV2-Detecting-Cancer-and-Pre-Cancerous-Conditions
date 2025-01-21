# Clasificación de Lesiones de Piel usando MobileNetV2 🩺📸

Este proyecto utiliza un modelo basado en **MobileNetV2** para clasificar lesiones de piel en cuatro categorías:
- **Melanoma (MEL)**
- **Carcinoma Basocelular (BCC)**
- **Queratosis Actínica (AKIEC)**
- **Sin Cáncer**

El modelo se entrenó con el [Dataset HAM10000](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T), que contiene imágenes de lesiones de piel etiquetadas por dermatólogos.

---

## 🚀 Características Principales
- **MobileNetV2 como Modelo Base**: Utiliza una arquitectura ligera y eficiente para clasificación de imágenes.
- **Preprocesamiento de Imágenes**: Redimensiona las imágenes a 224x224 píxeles, normaliza los valores de píxeles y las prepara para el modelo.
- **Predicción Fácil de Usar**: Sube una imagen y el modelo predecirá el tipo de lesión.
- **Resultados Visuales**: Muestra la imagen junto con la clase predicha y el nivel de confianza.

---

## 📂 Notebook de Google Colab
Puedes ejecutar este proyecto directamente en Google Colab haciendo clic en el botón de abajo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Fr4ndev/Skin-Lesion-Classification-using-MobileNetV2-Detecting-Cancer-and-Pre-Cancerous-Conditions.ipynb)

---

## 🛠️ ¿Cómo Funciona?
1. **Preprocesamiento**:
   - Las imágenes se redimensionan a 224x224 píxeles.
   - Los valores de píxeles se normalizan al rango [0, 1].
   - Se añade una dimensión extra para que el modelo pueda procesarlas.

2. **Arquitectura del Modelo**:
   - **MobileNetV2** como modelo base (preentrenado en ImageNet).
   - Capas adicionales:
     - Global Average Pooling.
     - Capa densa con 128 unidades y activación ReLU.
     - Capa de Dropout para evitar sobreajuste.
     - Capa de salida con 4 unidades y activación Softmax.

3. **Entrenamiento**:
   - El modelo se entrena usando el optimizador Adam y la función de pérdida de entropía cruzada categórica.
   - Logra una alta precisión en el conjunto de prueba.

4. **Predicción**:
   - Sube una imagen y el modelo predice la clase (por ejemplo, Melanoma, Sin Cáncer, etc.).
   - Los resultados se muestran visualmente junto con la imagen y la predicción.

---

## 🖥️ Uso en Google Colab
1. Abre el notebook en Google Colab usando el botón de arriba.
2. Ejecuta las celdas en orden:
   - **Instalar Dependencias**: Instala TensorFlow y otras librerías necesarias.
   - **Cargar el Dataset**: Descarga y prepara el dataset HAM10000.
   - **Entrenar el Modelo**: Entrena el modelo basado en MobileNetV2.
   - **Hacer Predicciones**: Sube una imagen y observa la predicción del modelo.

---


## 📝 Requisitos
El notebook instala automáticamente todas las dependencias necesarias. Sin embargo, esto es lo que necesitarás:
- Python 3.8+
- TensorFlow 2.x
- NumPy
- Pandas
- Matplotlib
- PIL (Pillow)

---

## 🤝 Contribuciones
¡Las contribuciones son bienvenidas! Si deseas mejorar el modelo, agregar nuevas características o corregir errores, no dudes en abrir un issue o enviar un pull request.

---

## 📜 Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

---

## 🙏 Agradecimientos
- Al [Dataset HAM10000](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T) por proporcionar las imágenes de lesiones de piel.
- A TensorFlow y Keras por el framework de deep learning.
- A MobileNetV2 por la arquitectura ligera y eficiente.

