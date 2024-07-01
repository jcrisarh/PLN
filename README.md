# Desafíos de Procesamiento de Texto

Este repositorio contiene cinco desafíos de Procesamiento de Lenguaje Natural (NLP) implementados en forma de notebooks interactivos en Python. 

## Desafío 1: Vectorización de texto y modelo de clasificación Naïve Bayes con el dataset 20 newsgroups

El objetivo de este desafío es explorar la vectorización de documentos y medir la similaridad entre ellos. 

### Objetivos y Análisis

1. Se vectorizan documentos utilizando diferentes técnicas de representación de texto. Se seleccionan al azar 5 documentos y se mide la similaridad con el resto de los documentos del conjunto de datos. Posteriormente, se analizan los 5 documentos más similares de cada uno para evaluar si la similaridad tiene sentido en relación con el contenido del texto y las etiquetas de clasificación asociadas.

2. Se entrenan modelos de clasificación Naïve Bayes con el objetivo de maximizar el desempeño de clasificación, medido mediante el f1-score macro en el conjunto de datos de prueba. Se considera la optimización de parámetros tanto para el vectorizador como para los modelos Naïve Bayes (Multinomial y ComplementNB), explorando cómo estos cambios afectan el rendimiento del modelo.

3. Se transpone la matriz documento-término para obtener una matriz término-documento. Con esta representación, se estudia la similaridad entre palabras seleccionando 5 palabras y analizando sus 5 palabras más similares según la representación vectorial. Este análisis permite explorar cómo las palabras se agrupan semánticamente en función de su contexto en los documentos.

### Archivos Incluidos

- `Desafio_1.ipynb`

## Desafío 2: Custom Embeddings con Gensim

En este desafío, se explorará la creación de vectores personalizados utilizando Gensim basado en un e-book obtenido de Project Gutenberg.

### Objetivos y Análisis

1. **Creación de Vectores con Gensim:**
   - Se utiliza Gensim para entrenar vectores de palabras (embeddings) a partir del e-book proporcionado.
   - Se aplica la técnica Word2Vec para generar representaciones vectoriales de términos del e-book.

2. **Análisis de Similitudes y Diferencias:**
   - Se seleccionan términos de interés y se exploran sus similitudes y diferencias en el espacio de embeddings.
   - Se comparar cómo se relacionan semánticamente los términos.

3. **Visualización:**
   - Se grafican los embeddings para visualizar la distribución de los términos en un espacio dimensional reducido.

### Datos

Los datos utilizados provienen del siguiente e-book de Project Gutenberg:

- **Título:** Introduction to the study of the history of language
- **Autores:** Herbert A. Strong, Willem Sijbrand Logeman, Benjamin Ide Wheeler
- **Fecha de Publicación:** 8 de enero de 2019
- **Idioma:** Inglés

### Archivos Incluidos

- `Desafio_2.ipynb`:  Notebook que aborda el segundo desafío del proyecto.

#### Carpeta `docs`

- `Introduction_to_the_study_of_the_history_of_language.txt`: Texto completo del e-book utilizado para entrenar los embeddings.
- `cleaned_text.txt`: Versión procesada del e-book, con partes irrelevantes eliminadas.

#### Carpeta `images`: Archivos HTML que contienen visualizaciones o información adicional relevante para el proyecto.

- 

## Desafío 3: Modelo de Lenguaje con Tokenización por Palabras

En este desafío, se implementará un modelo de lenguaje utilizando tokenización por palabras y arquitecturas de redes neuronales recurrentes.

### Pasos y Consideraciones

1. **Selección del Corpus:**
   - Seleccionar un corpus de texto adecuado para entrenar el modelo de lenguaje. Puede ser un conjunto de libros, artículos o cualquier fuente de texto extensa.

2. **Pre-procesamiento y Tokenización:**
   - Realizar el pre-procesamiento necesario para tokenizar el corpus y estructurar el dataset.
   - Separar los datos entre conjuntos de entrenamiento y validación para evaluar el desempeño del modelo.

3. **Arquitecturas de Redes Neuronales Recurrentes:**
   - Proponer y evaluar diferentes arquitecturas de redes neuronales recurrentes como SimpleRNN (celda de Elman), LSTM y GRU para implementar el modelo de lenguaje.
   - Utilizar el optimizador rmsprop u otros optimizadores para la convergencia del modelo.

4. **Generación de Nuevas Secuencias:**
   - Implementar estrategias de generación de texto como greedy search y beam search (determinístico y estocástico) utilizando el modelo entrenado.
   - Observar el efecto de la temperatura en la generación de secuencias estocásticas para controlar la creatividad del modelo.

### Archivos Incluidos

- `tokenizacion.py`: Script para el pre-procesamiento y tokenización del corpus.
- `modelo_rnn.py`: Implementación de modelos de redes neuronales recurrentes (SimpleRNN, LSTM, GRU).
- `generacion_texto.ipynb`: Notebook Jupyter con la implementación de generación de nuevas secuencias utilizando el modelo entrenado.

## Desafío 4: LSTM Bot QA con datos del challenge ConvAI2

En este desafío, se implementará un modelo basado en LSTM para construir un BOT capaz de responder preguntas del usuario utilizando datos del challenge ConvAI2.

### Datos

Los datos utilizados provienen del challenge ConvAI2, que incluye conversaciones en inglés diseñadas para evaluar la inteligencia conversacional de los sistemas. Puedes acceder a los datos en el siguiente enlace:

- [ConvAI2 Challenge Data](link_al_dataset)

### Objetivo

1. **Construcción del BOT QA:**
   - Utilizar modelos LSTM para construir un BOT capaz de responder preguntas formuladas por usuarios en base a las conversaciones del dataset ConvAI2.

2. **Pre-procesamiento de Datos:**
   - Realizar el pre-procesamiento adecuado para limpiar y estructurar los datos del challenge ConvAI2.
   - Separar los datos en conjuntos de entrenamiento y prueba para entrenar y evaluar el modelo.

3. **Implementación de LSTM:**
   - Implementar un modelo LSTM utilizando bibliotecas como TensorFlow, PyTorch o Keras para el procesamiento de secuencias y la generación de respuestas coherentes.

4. **Evaluación y Ajuste:**
   - Evaluar el desempeño del BOT QA utilizando métricas relevantes como precisión, recall y F1-score para respuestas generadas.
   - Realizar ajustes en la arquitectura del modelo y en los hiperparámetros para mejorar la calidad de las respuestas.

### Archivos Incluidos

- `preprocesamiento.py`: Script para el pre-procesamiento y estructuración de los datos del dataset ConvAI2.
- `modelo_lstm.py`: Implementación del modelo LSTM para la construcción del BOT QA.
- `evaluacion_modelo.ipynb`: Notebook Jupyter con la evaluación del desempeño del modelo y análisis de respuestas generadas.

