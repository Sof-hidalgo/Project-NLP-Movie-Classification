# Project-NLP-Movie-Classification

# 📌 Film Junky Union - Clasificación de Reseñas de Películas

## 📖 Descripción del Proyecto
Film Junky Union, una comunidad de aficionados al cine clásico, necesitaba un sistema para filtrar y categorizar automáticamente las reseñas de películas. Se construyó un modelo de Machine Learning utilizando un conjunto de datos de reseñas de IMDB con etiquetas de polaridad, con el objetivo de clasificar las opiniones en positivas y negativas de manera eficiente.

## 🎯 Objetivo del Proyecto
Entrenar un modelo de Machine Learning para la clasificación automática de reseñas de películas, asegurando un F1-Score mínimo de 0.85 para lograr una precisión adecuada en la identificación de críticas negativas.

### Descripción de los datos
Los datos se almacenan en el archivo imdb_reviews.tsv. Descargar el conjunto de datos.

Los datos fueron proporcionados por Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, y Christopher Potts. (2011). Learning Word Vectors for Sentiment Analysis. La Reunión Anual 49 de la Asociación de Lingüística Computacional (ACL 2011).

Aquí se describen los campos seleccionados:

- review: el texto de la reseña
- pos: el objetivo, '0' para negativo y '1' para positivo
- ds_part: 'entrenamiento'/'prueba' para la parte de entrenamiento/prueba del conjunto de datos, respectivamente

## 📊 Conclusiones Finales
- Se probaron varios enfoques, incluyendo TF-IDF con Regresión Logística y LightGBM, y modelos basados en SpaCy.
- El mejor modelo fue SpaCy + Regresión Logística, con un F1-Score de 0.87 y un AUC-ROC de 0.95, superando los otros métodos.
- TF-IDF mostró limitaciones al no captar el significado contextual de las palabras, alcanzando un F1-Score máximo de 0.56.
- El modelo se probó con reseñas nuevas, demostrando buena capacidad de generalización, aunque con algunas dificultades en textos ambiguos.
- Conclusión general: El modelo entrenado es adecuado para la tarea y podría implementarse en un sistema automatizado de clasificación de reseñas.

## 🛠 Skills Obtenidas
- Procesamiento de lenguaje natural (NLP) con TF-IDF y SpaCy.
- Implementación de modelos de Regresión Logística y LightGBM.
- Evaluación de modelos con métricas como F1-Score, AUC-ROC, precisión y recall.
- Análisis exploratorio de datos (EDA) para identificar patrones en las reseñas de películas.
- Prueba de modelos con nuevas reseñas para evaluar su desempeño en casos reales.

## 💡 Lecciones Aprendidas
- Preprocesamiento eficiente: El uso de SpaCy y la lematización mejoró significativamente la clasificación.
- Elección del modelo: Modelos simples como la Regresión Logística pueden superar a modelos más complejos, dependiendo de los datos.
- Limitaciones computacionales: Modelos avanzados como BERT no pudieron implementarse debido a restricciones de hardware.
- Balance de clases: Tener un dataset equilibrado facilitó la clasificación sin necesidad de técnicas de resampling.
- Evaluación con reseñas reales: Es importante probar los modelos con datos externos para validar su efectividad en un entorno real.
