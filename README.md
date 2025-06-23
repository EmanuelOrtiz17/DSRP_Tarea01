# 🧠 Proyectos de Especialización en Machine Learning Engineering

Este repositorio contiene dos proyectos desarrollados como parte del curso I de la especialización en Machine Learning Engineering. Ambos abordan problemas reales aplicando principios de programación orientada a objetos, buenas prácticas de ingeniería de software y fundamentos de Machine Learning.

---

## 📚 Tabla de Contenidos

- [🎯 Objetivo General](#-objetivo-general)
- [📁 Proyecto 1: Clasificación de Cáncer de Mama](#-proyecto-1-clasificación-de-cáncer-de-mama)
  - [Definición del Problema](#definición-del-problema)
  - [Descripción del Dataset](#descripción-del-dataset)
  - [🛠️ Tecnologías Utilizadas](#️-tecnologías-utilizadas)
  - [📖 Diccionario de Datos](#-diccionario-de-datos)
  - [📄 Model Card](#-model-card)
  - [📊 Resultados](#-resultados)
  - [🧩 Conclusiones](#-conclusiones)
- [📁 Proyecto 2: Clasificación de Color y Forma de Objetos](#-proyecto-2-clasificación-de-color-y-forma-de-objetos)
  - [Definición del Problema](#definición-del-problema-1)
  - [Descripción del Dataset](#descripción-del-dataset-1)
  - [🛠️ Tecnologías Utilizadas](#️-tecnologías-utilizadas-1)
  - [📄 Model Card](#-model-card-1)
  - [📊 Resultados](#-resultados-1)
  - [🧩 Conclusiones](#-conclusiones-1)

---

## 🎯 Objetivo General

Aplicar conocimientos teóricos y prácticos en Machine Learning para resolver problemas reales, estructurando proyectos escalables y mantenibles mediante principios de ingeniería de software como POO y SOLID.

---

## 📁 Proyecto 1: Clasificación de Cáncer de Mama

### Definición del Problema

Construir un modelo de clasificación supervisado para diagnosticar si un tumor de mama es maligno o benigno utilizando el dataset **Breast Cancer Wisconsin (Diagnostic)**.

### Descripción del Dataset

- Fuente: [Scikit Learn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)
- Instancias: 569
- Características: 30 variables numéricas (todas reales y positivas)
- Etiquetas: 2 clases (malignant = maligno, benign = benigno)
- Formato: Matriz de datos de forma (569, 30) y vector objetivo de forma (569,)
- Fuente original: UCI ML Repository
- Uso en Scikit-learn: from sklearn.datasets import load_breast_cancer

### 🛠️ Tecnologías Utilizadas

- Python 3.x: Lenguaje de programación principal.
- Jupyter Notebook: Entorno interactivo para desarrollo y documentación del código.
- Scikit-learn (sklearn): Biblioteca de aprendizaje automático utilizada para:
- Cargar el dataset (datasets.load_breast_cancer)
- Entrenar el modelo (SVC)
- Dividir los datos (train_test_split)
- Evaluar el modelo (accuracy_score, confusion_matrix, classification_report)
- NumPy: Para manipulación de arrays numéricos.


### 📖 Diccionario de Datos

El dataset **Breast Cancer Wisconsin (Diagnostic)** contiene 30 características numéricas extraídas de imágenes digitales de aspirados con aguja fina (FNA) de masas mamarias. Estas características describen propiedades de los núcleos celulares.

Cada característica se calcula en tres versiones: **media**, **error estándar** y **valor “peor”** (mayor valor entre los tres peores núcleos).

| Categoría         | Característica                  | Descripción                                                                 |
|-------------------|----------------------------------|-----------------------------------------------------------------------------|
| Forma             | `radius`                        | Promedio de distancias del centro al perímetro                             |
| Textura           | `texture`                       | Desviación estándar de los valores de escala de grises                     |
| Forma             | `perimeter`                     | Perímetro de la masa                                                        |
| Área              | `area`                          | Área de la masa                                                             |
| Suavidad          | `smoothness`                    | Variación local en la longitud del radio                                   |
| Compacidad        | `compactness`                   | (perímetro² / área) - 1.0                                                  |
| Concavidad        | `concavity`                     | Severidad de las partes cóncavas del contorno                              |
| Puntos cóncavos   | `concave points`                | Número de partes cóncavas del contorno                                     |
| Simetría          | `symmetry`                      | Simetría del núcleo                                                         |
| Dimensión fractal | `fractal dimension`             | Aproximación de la dimensión fractal del contorno                          |

Cada una de estas características aparece como:

- `mean`: valor promedio
- `se`: error estándar
- `worst`: valor máximo entre los tres peores núcleos

**Variable objetivo (`target`)**:
- `0`: Maligno
- `1`: Benigno


### 📄 Model Card

**Modelo:** Support Vector Classifier (SVC) con kernel RBF (por defecto)  
**Métrica principal:** Accuracy, Precision, Recall, F1-score  
**Uso previsto:** Diagnóstico médico asistido para clasificación de tumores de mama

⚠️ Limitaciones:
- No sustituye diagnóstico clínico profesional  
- Sensible a la escala de los datos (**no se aplicó normalización**)  
- Tendencia a clasificar en exceso como benigno (ver matriz de confusión)


## 📊 Resultados

**Accuracy:** 93.6%

### Precision:
- **Clase 0 (Maligno):** 1.00  
- **Clase 1 (Benigno):** 0.91

### Recall:
- **Clase 0 (Maligno):** 0.83  
- **Clase 1 (Benigno):** 1.00

### F1-score:
- **Clase 0 (Maligno):** 0.90  
- **Clase 1 (Benigno):** 0.95

### Matriz de Confusión:

|               | Predicho Maligno | Predicho Benigno |
|---------------|------------------|------------------|
| **Real Maligno** | 52               | 11               |
| **Real Benigno** | 0                | 108              |

---

 🔍 Observaciones:

- El modelo clasificó correctamente todos los casos benignos.  
- Se cometieron **11 falsos negativos** (malignos clasificados como benignos), lo cual es crítico en contextos médicos.

---

## 🧠 Conclusiones

- El modelo **SVC** alcanzó una precisión general alta (**93.6%**), pero mostró un **recall bajo para la clase maligna**, lo cual puede ser riesgoso en aplicaciones clínicas.  
- Se recomienda aplicar **normalización de datos** y **ajustar hiperparámetros** para mejorar la sensibilidad del modelo.  
- La implementación demuestra un flujo completo de *Machine Learning* supervisado, desde la **carga de datos** hasta la **evaluación**, siguiendo buenas prácticas de ingeniería.


---

## 📁 Proyecto 2: Clasificación de Color y Forma de Objetos

### Definición del Problema

Desarrollar un modelo basado en un Perceptrón Multicapa (MLP) para clasificar objetos en imágenes según su color y forma.

### 📦 Descripción del Dataset

- Dataset propio o generado artificialmente
- Atributos: características extraídas de imágenes (color en espacio HSV y forma mediante momentos de Hu)
- Etiquetas: combinaciones como `"círculo rojo"`, `"cuadrado azul"`, etc.
- Tamaño del dataset:
  - **Color**: 27 imágenes de entrenamiento, 9 de prueba
  - **Forma**: 12 imágenes de entrenamiento, 9 de prueba

---

### 🛠️ Tecnologías Utilizadas

- Python 3.x
- Scikit-learn (MLPClassifier)
- OpenCV (cv2) para procesamiento de imágenes
- PIL (Python Imaging Library)
- Matplotlib y NumPy
- Scikit-image (skimage)
- Git & GitHub
- Principios SOLID y POO

---

### 📄 Model Card

- **Modelo:** Perceptrón Multicapa (MLP)
  - Color: `hidden_layer_sizes=(16, 11)`
  - Forma: `hidden_layer_sizes=(10, 6)`
- **Métrica principal:** Accuracy
- **Uso previsto:** Clasificación visual básica de objetos por color y forma
- **Limitaciones:**
  - Dataset pequeño y artificial
  - No robusto a ruido, rotaciones extremas o condiciones de iluminación variables
  - El modelo no fue escalado ni optimizado con técnicas de regularización avanzadas

---

### 📊 Resultados

#### Clasificador de Color:
- **Accuracy:** 100%
- **Matriz de Confusión:**
  [[3 0 0]
   [0 3 0]
   [0 0 3]]
- **Predicciones correctas:** 9/9

#### Clasificador de Forma:
- **Accuracy:** 100%
- **Matriz de Confusión:**
  [[3 0 0]
   [0 3 0]
   [0 0 3]]
- **Predicciones correctas:** 9/9

---

### 🧠 Conclusiones

- El modelo MLP logró clasificar correctamente todas las imágenes tanto por color como por forma.
- Se utilizaron descriptores simples pero efectivos: HSV para color y momentos de Hu para forma.
- El pipeline demuestra una implementación clara de un sistema de clasificación visual básico.
- Se recomienda escalar el dataset y aplicar validación cruzada para evaluar la generalización.
- El uso de buenas prácticas como funciones modulares y separación de entrenamiento/prueba facilita la mantenibilidad del código.

---





