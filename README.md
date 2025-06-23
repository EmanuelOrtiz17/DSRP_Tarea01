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

- Fuente: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- Instancias: 569
- Atributos: 30 características numéricas + 1 etiqueta (diagnóstico)

### 🛠️ Tecnologías Utilizadas

- Python 3.x
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn
- Git & GitHub
- Principios SOLID y POO

### 📖 Diccionario de Datos

| Variable       | Descripción                          |
|----------------|--------------------------------------|
| radius_mean    | Promedio del radio de las células    |
| texture_mean   | Promedio de la textura               |
| ...            | ...                                  |
| diagnosis      | Diagnóstico (M = maligno, B = benigno)|

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





