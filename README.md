# 🧠 Proyectos de Especialización en Machine Learning Engineering

Este repositorio contiene dos proyectos desarrollados como parte del curso I de la especialización en Machine Learning Engineering. Ambos abordan problemas reales aplicando principios de programación orientada a objetos, buenas prácticas de ingeniería de software y fundamentos de Machine Learning.

---

## 📚 Tabla de Contenidos

- [🎯 Objetivo General](#-objetivo-general)
- [📁 Proyecto 1: Clasificación de Cáncer de Mama](#-proyecto-1-clasificación-de-cáncer-de-mama)
  - [Definición del Problema](#definición-del-problema)
  - [Diagrama de Flujo](#diagrama-de-flujo)
  - [Descripción del Dataset](#descripción-del-dataset)
  - [🛠️ Tecnologías Utilizadas](#️-tecnologías-utilizadas)
  - [📖 Diccionario de Datos](#-diccionario-de-datos)
  - [📄 Model Card](#-model-card)
  - [📊 Resultados](#-resultados)
  - [🧩 Conclusiones](#-conclusiones)
- [📁 Proyecto 2: Clasificación de Color y Forma de Objetos](#-proyecto-2-clasificación-de-color-y-forma-de-objetos)
  - [Definición del Problema](#definición-del-problema-1)
  - [Diagrama de Flujo](#diagrama-de-flujo-1)
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

### Diagrama de Flujo

_(Aquí se incluirá un diagrama visual del flujo del proyecto)_

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

- **Modelo:** Clasificador supervisado (Random Forest, SVM, etc.)
- **Métrica principal:** Accuracy, Precision, Recall, F1-score
- **Uso previsto:** Diagnóstico médico asistido
- **Limitaciones:** No sustituye diagnóstico clínico profesional

### 📊 Resultados

- Accuracy: XX%
- Precision: XX%
- Recall: XX%
- F1-score: XX%

_(Incluir gráficos como matriz de confusión, curva ROC, etc.)_

### 🧩 Conclusiones

- El modelo logra una buena capacidad de generalización.
- Se identificaron las características más relevantes.
- Se aplicaron principios de ingeniería para asegurar escalabilidad.

---

## 📁 Proyecto 2: Clasificación de Color y Forma de Objetos

### Definición del Problema

Desarrollar un modelo basado en un Perceptrón Multicapa (MLP) para clasificar objetos en imágenes según su color y forma.

### Diagrama de Flujo

_(Aquí se incluirá un diagrama visual del flujo del proyecto)_

### Descripción del Dataset

- Dataset propio o generado artificialmente
- Atributos: características extraídas de imágenes (color, forma)
- Etiquetas: combinaciones como "círculo rojo", "cuadrado azul", etc.

### 🛠️ Tecnologías Utilizadas

- Python 3.x
- Scikit-learn o Keras (según implementación)
- OpenCV o PIL (para procesamiento de imágenes)
- Git & GitHub
- Principios SOLID y POO

### 📄 Model Card

- **Modelo:** Perceptrón Multicapa (MLP)
- **Métrica principal:** Accuracy
- **Uso previsto:** Clasificación visual básica
- **Limitaciones:** Dataset limitado, no robusto a ruido visual

### 📊 Resultados

- Accuracy: XX%
- Ejemplos de predicciones correctas e incorrectas

### 🧩 Conclusiones

- El MLP logra distinguir combinaciones básicas de color y forma.
- Se aplicaron buenas prácticas de ingeniería para facilitar mantenimiento y escalabilidad.

---





