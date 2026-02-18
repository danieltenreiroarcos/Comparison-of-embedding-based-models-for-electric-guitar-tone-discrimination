# 🎸🧠 Comparativa de modelos basados en embeddings para la discriminación del tono de la guitarra eléctrica
## 🎓 Trabajo Fin de Estudios — Máster en Inteligencia Artificial (UNIR)

### 👤 Autor
Daniel Tenreiro Arcos  
LinkedIn: https://www.linkedin.com/in/danieltenreiro/

---

## 📌 Descripción
Este repositorio contiene el desarrollo experimental del Trabajo Fin de Estudios centrado en la comparación de modelos de representación de audio basados en deep learning para el análisis de tono en guitarra eléctrica.

El objetivo principal es evaluar hasta qué punto modelos de embeddings musicales preentrenados capturan información tímbrica relevante, diferenciando configuraciones de tono (pastillas, amplificación y cadena de señal) más allá de variaciones de interpretación o pitch.

El trabajo se enfoca en:
- ✅ Análisis cuantitativo mediante recuperación por similitud (Top-K)
- 🧭 Estudio estructural del espacio latente (t-SNE, matrices de confusión, etc.)

---

## 🎯 Objetivos
- 📈 Evaluar el comportamiento de distintos modelos de embeddings en tareas de recuperación basada en similitud.
- 🥇🥈 Comparar métricas Top-1 y Top-5 sobre conjuntos de validación independientes.
- 🧬 Analizar la separabilidad del espacio latente mediante técnicas de reducción de dimensionalidad.
- 🛠️ Estudiar el impacto del fine-tuning frente al uso de modelos congelados.
- 🧠 Determinar qué arquitectura captura mejor información tímbrica específica.

---

## 🤖 Modelos evaluados
- 🎼 **MERT (Music Embedding Representation Transformer)** (MERT-v1-330M)
- 🔊 **PANNs (Pretrained Audio Neural Networks)** (CNN14)

Cada modelo se evaluó bajo diferentes configuraciones:
- 🕒 Extracción de embeddings globales mediante pooling temporal.
- 📉 Versiones proyectadas vs. representaciones de alta dimensionalidad.
- 🔧 Configuraciones con y sin fine-tuning parcial.
- 🧪 Separación explícita train/validation para evitar fuga de información.

---

## 🧪 Metodología (pipeline)
Flujo experimental general:
1. 🎧 Extracción de embeddings a partir de audio procesado
2. 📏 Normalización de vectores
3. 📐 Similitud coseno entre muestras
4. 🔎 Evaluación mediante recuperación Top-K (Top-1 / Top-5)
5. 🧾 Matrices de confusión
6. 🗺️ Visualización del espacio latente (t-SNE)
7. 🧷 Comparación baseline vs. fine-tuning

📌 Las métricas se calcularon **exclusivamente sobre el conjunto de validación** para garantizar consistencia metodológica.

---

## 🧰 Librerías principales

Las principales librerías utilizadas a lo largo de los notebooks experimentales son:

- **Procesamiento numérico y de datos**:
  - `numpy`
  - `pandas`

- **Visualización**:
  - `matplotlib`

- **Aprendizaje automático y evaluación**:
  - `scikit-learn`

- **Framework de Deep Learning**:
  - `torch` (PyTorch)
  - `torchaudio`

- **Implementación de modelos**:
  - `transformers`
  - `panns_inference`

- **Procesamiento de audio**:
  - `soundfile`

- **Utilidades**:
  - `tqdm`

---

# 🎸🧠 Comparative Study of Embedding-Based Models for Electric Guitar Tone Discrimination
## 🎓 Final Master’s Project — Master’s Degree in Artificial Intelligence (UNIR)

### 👤 Author
Daniel Tenreiro Arcos  
LinkedIn: https://www.linkedin.com/in/danieltenreiro/

---

## 📌 Description
This repository contains the experimental development of the Final Master’s Project focused on comparing deep learning-based audio representation models for electric guitar tone analysis.

The main objective is to evaluate to what extent pretrained musical embedding models capture relevant timbral information, discriminating tone configurations (pickups, amplification, and signal chain) beyond variations in performance or pitch.

The work focuses on:
- ✅ Quantitative analysis through similarity-based retrieval (Top-K)
- 🧭 Structural study of the latent space (t-SNE, confusion matrices, etc.)

---

## 🎯 Objectives
- 📈 Evaluate the behavior of different embedding models in similarity-based retrieval tasks.
- 🥇🥈 Compare Top-1 and Top-5 metrics on independent validation sets.
- 🧬 Analyze latent space separability using dimensionality reduction techniques.
- 🛠️ Study the impact of fine-tuning compared to frozen models.
- 🧠 Determine which architecture better captures timbre-specific information.

---

## 🤖 Evaluated Models
- 🎼 **MERT (Music Embedding Representation Transformer)** (MERT-v1-330M)
- 🔊 **PANNs (Pretrained Audio Neural Networks)** (CNN14)

Each model was evaluated under different configurations:
- 🕒 Extraction of global embeddings using temporal pooling.
- 📉 Projected versions vs. high-dimensional representations.
- 🔧 Configurations with and without partial fine-tuning.
- 🧪 Explicit train/validation split to prevent data leakage.

---

## 🧪 Methodology (pipeline)
General experimental workflow:
1. 🎧 Extraction of embeddings from processed audio
2. 📏 Vector normalization
3. 📐 Cosine similarity computation between samples
4. 🔎 Evaluation using Top-K retrieval (Top-1 / Top-5)
5. 🧾 Confusion matrices
6. 🗺️ Latent space visualization (t-SNE)
7. 🧷 Baseline vs. fine-tuned comparison

📌 Metrics were computed **exclusively on the validation set** to ensure methodological consistency.

---

## 🧰 Main Libraries

The main libraries used throughout the experimental notebooks are:

- **Numerical & Data Processing**:
  - `numpy`
  - `pandas`

- **Visualization**:
  - `matplotlib`

- **Machine Learning & Evaluation**:
  - `scikit-learn`

- **Deep Learning Framework**:
  - `torch` (PyTorch)
  - `torchaudio`

- **Model Implementations**:
  - `transformers`
  - `panns_inference`

- **Audio Processing**:
  - `soundfile`

- **Utilities**:
  - `tqdm`

