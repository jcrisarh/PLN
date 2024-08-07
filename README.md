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
   - Se seleccionan términos de interés y se exploran sus similitudes y diferencias en el espacio de embeddings. Se comparan cómo se relacionan semánticamente los términos.

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

- `caso['accusative', 'genitive'].html`
- `caso['nouns', 'verbs'].html`
- `caso['object', 'predicate', 'subject'].html`
- `caso['often', 'sometimes'].html`
- `caso['past', 'present'].html`
- `caso['speak', 'say'].html`
- `caso['substantive', 'noun'].html`
- `caso['substantive', 'subject', 'noun', 'object', 'predicate'].html`
- `embedding2d_visualization.html`
- `embedding3d_visualization.html`

![embedding3d](https://github.com/jcrisarh/PLN/blob/master/desafio_2/images/embedding3d_visualization.html)

## Desafío 3: Modelo de Lenguaje con Tokenización por Palabras y Caracteres

En este desafío, se implementará un modelo de lenguaje utilizando tokenización por palabras y caractéres y 3 arquitecturas: SimpleRNN, LSM y GRU.

### Objetivos y Análisis

1. **Selección del corpus, pre-procesamiento y tokenización:**
   - Se selecciona un corpus de texto proveniente de  un e-book de proyecto Gutenberg.
   - Se reazliza la limpieza del corpus y la tokenización para estructurar el dataset. Se separan los datos en entrenamiento y validación.

2. **Modelado y entrenamiento:**
   - Se evaluan 3 arquitecturas diferentes para implementar el modelo de lenguaje con el optimizador rmsprop.

3. **Generación de Nuevas Secuencias:**
   - Se implementan las estrategias de generación de texto greedy search y beam search.

### Datos

Los datos utilizados provienen del siguiente e-book de Project Gutenberg:

- **Título:** The Happy Prince, and Other Tales
- **Autores:** Oscar Wilde
- **Fecha de Publicación:** Marzo de 1910
- **Idioma:** Inglés

     

### Archivos Incluidos

- `Desafio3_char.ipynb`, `Desafio3_word.ipynb`: Notebooks para la implementación de los modelos de lenguaje por caracteres y palabras.
- `GRU_character`, `GRU_word`, `LSTM_character`, `LSTM_word`, `SIMPLERNN_character`, `SIMPLERNN_word`, `GRU2_character.keras`, `LSTM2_character.keras` : Modelos entrenados.

#### Carpeta `docs`:
- `the_happy_prince_and_other_tales`: Texto completo proveniente del e-book utilizado.
- `cleaned_text.txt`: Texto procesado para modelo de lenguaje por caracteres.
- `cleaned_text2.txt`: Texto procesado para modelo de lenguaje por palabras.

#### Carpeta `images`:
- Imágenes png de gradio para predecir la próxima palabra o caracter según corresponda al testear diferentes modelos.

  ![ejemplo gradio](https://github.com/jcrisarh/PLN/blob/master/desafio_3/images/char1gru.png)


  

## Desafío 4: LSTM Bot QA con datos del challenge ConvAI2

En este desafío, se implementa un modelo basado en LSTM para construir un BOT capaz de responder preguntas del usuario utilizando datos del challenge ConvAI2.

### Datos

Los datos utilizados provienen del challenge ConvAI2, que incluye conversaciones en inglés diseñadas para evaluar la inteligencia conversacional de los sistemas. Se puede acceder acceder a los datos en el siguiente enlace:

- [ConvAI2 Challenge Data](http://convai.io/data/)

### Objetivos y Análisis

- Se realiza el pre-procesamiento adecuado para limpiar y estructurar los datos del challenge ConvAI2.
- Se tokenizan las preguntas y respuestas.
- Se separan los datos en conjuntos de entrenamiento y prueba para entrenar y evaluar el modelo.
- Se utiliza un modelo LSTM para construir el bot conversacional.

### Archivos Incluidos

- `6-bot_qa.ipynb`: Notebook para el preprocesamiento de datos y la construcción del bot.
- `data_volunteers.json`: Archivo json que contiene los datos.
- `model_plot.png`,`encoder_plot.png`,`decoder_plot.png` : Gráficos generados de los modelos.


## Desafío 5: Bert Sentiment Analysis
En este desafío se implementa un modelo Bert para Sentiment Analysis.

### Datos

Se utiliza como dataset las críticas de Google Apps en formato csv.

### Objetivos y Análisis
- Se entrena un modelo Bert para clasificacion de tres clases: Positivo, Neutral y Negativo, obtenido a partir de 5 clases originales.
- Se entrena el modelo con las 5 clases originales: 1, 2, 3, 4 y 5.
- Se añade una capa densa para el entrenamiento de las 5 clases originales.

### Archivos Incluidos
- `desafio_5.ipynb`: Notebook para el entrenamiento de Bert para sentiment analysis.
- `apps.csv`, `reviews.csv`: Archivos parte del dataset
  


