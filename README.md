# 🐋 Clasificación de Ballenas por Imagen

Este repositorio contiene un proyecto de clasificación multiclase extrema aplicado al reconocimiento de especies de ballenas a partir de imágenes. Utiliza técnicas de visión por computadora y aprendizaje profundo para abordar un problema con más de 4000 clases altamente desbalanceadas.

---

## 📚 Estructura del Proyecto

El trabajo se organiza en tres notebooks principales, que siguen el flujo típico de un proyecto de Machine Learning:

### 🔍 1. `01_exploración_de_datos.ipynb`
- Carga del dataset y análisis exploratorio inicial.
- Visualización de la cantidad de imágenes por clase (`Id`).
- Análisis de la distribución de resoluciones de las imágenes.
- Identificación de desbalance severo entre clases.

### 🧼 2. `02_preprocesado.ipynb`
- Lectura y transformación de imágenes: redimensionamiento, normalización y conversión a arrays NumPy.
- División en conjuntos de entrenamiento y validación (80% - 20%).
- Codificación de etiquetas con `LabelEncoder`.
- Validación de shapes y balance de clases por subconjunto.

### 🧠 3. `03_arquitectura_de_linea_de_base.ipynb`
- Definición de un modelo CNN básico como línea base.
- Entrenamiento con optimizador Adam y función de pérdida `categorical_crossentropy`.
- Visualización de curvas de precisión y pérdida.
- Evaluación preliminar del desempeño del modelo.

---

## 🌍 Contexto de Aplicación

La clasificación automática de especies de ballenas mediante imágenes forma parte de las aplicaciones emergentes de la inteligencia artificial en la biología marina, la gestión ambiental y la conservación de especies en peligro.

Tradicionalmente, la identificación de ballenas ha dependido de observaciones humanas o del análisis manual de fotografías, un proceso costoso y propenso a errores. La automatización con visión por computador permite analizar grandes volúmenes de imágenes con mayor precisión y eficiencia.

Esto facilita el monitoreo de las poblaciones, el seguimiento de sus patrones migratorios, y la identificación temprana de amenazas derivadas del cambio climático, la contaminación o las actividades humanas.

---

## 🎯 Objetivo del Proyecto

Predecir la especie de una ballena a partir de una imagen de entrada.  
Se trata de un **problema de clasificación supervisada** donde cada imagen JPEG está etiquetada con un identificador de especie (`Id`).

---

## 📂 Información del Dataset

- **Formato de los datos**: imágenes `.jpg` entre 170 KB y 1 MB.
- **Tamaño del conjunto**: 9850 imágenes (~289 MB).
- **Etiquetas**: variable `Id` representa la especie (4251 clases únicas).

### 📊 Distribución de clases
- Alta desbalance: unas pocas especies tienen cientos de imágenes, pero muchas otras tienen menos de 10.
- Las 30 especies más frecuentes concentran la mayoría de los ejemplos.
- Este desbalance presenta un reto significativo para los modelos de clasificación tradicionales.

---

## 📌 Resultados y consideraciones

- El modelo base alcanza una precisión de ~8.6%, lo que indica dificultades para generalizar.
- Las curvas de pérdida y precisión muestran **sobreajuste** y **baja capacidad de aprendizaje**, probablemente debido al desbalance de clases y a la escasez de datos por clase.
- Futuras mejoras incluyen: aumento de datos, arquitectura más robusta, y reformulación del problema como verificación (retrieval) en lugar de clasificación directa.

---

## 🚀 Autor
Este proyecto fue desarrollado como parte de una evaluación académica.  
- Andrés Peña
- Daniel Quiroz
- Luis Torres 

## Video explicativo
Youtube: https://youtu.be/-AVbJX7D798
