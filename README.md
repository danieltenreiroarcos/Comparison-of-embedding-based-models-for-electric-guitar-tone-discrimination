# Comparativa de modelos de IA para la representación de audio aplicada al análisis de tono de guitarra eléctrica

## Trabajo Fin de Estudios — Máster en Inteligencia Artificial (UNIR) - Autor: Daniel Tenreiro Arcos

### Descripción
Este repositorio contiene el desarrollo experimental del Trabajo Fin de Estudios centrado en la comparación de modelos de representación de audio basados en deep learning para el análisis de tono en guitarra eléctrica.
El objetivo principal del proyecto es evaluar hasta qué punto modelos de embeddings musicales preentrenados son capaces de capturar información tímbrica relevante, diferenciando configuraciones de tono (pastillas, amplificación y cadena de señal) más allá de variaciones de interpretación o pitch.
El trabajo se enfoca en análisis cuantitativo mediante tareas de recuperación por similitud y en el estudio estructural del espacio latente generado por distintos modelos.

### Objetivos

- Evaluar el comportamiento de distintos modelos de embeddings en tareas de recuperación basada en similitud.
- Comparar métricas Top-1 y Top-5 sobre conjuntos de validación independientes.
- Analizar la separabilidad del espacio latente mediante técnicas de reducción de dimensionalidad.
- Estudiar el impacto del fine-tuning frente al uso de modelos congelados.
- Determinar qué arquitectura captura mejor información tímbrica específica.

### Modelos evaluados

Se analizaron distintas arquitecturas de representación de audio, entre ellas:
- Music Embedding Representation Transformer (MERT)
- PANNs (Pretrained Audio Neural Networks)

Cada modelo se evaluó bajo diferentes configuraciones, incluyendo:
- Extracción de embeddings globales mediante pooling temporal.
- Versiones proyectadas frente a representaciones de alta dimensionalidad.
- Configuraciones con y sin fine-tuning parcial.
- Separación explícita train/validation para evitar fuga de información.

### Metodología

El flujo experimental general fue el siguiente:
- Extracción de embeddings a partir de audio procesado.
- Normalización de vectores.
- Cálculo de similitud coseno entre muestras.
- Evaluación mediante recuperación Top-K.
- Construcción de matrices de confusión.
- Visualización del espacio latente mediante t-SNE.
- Comparación entre configuraciones baseline y modelos ajustados.

Las métricas se calcularon exclusivamente sobre el conjunto de validación para garantizar consistencia metodológica.
