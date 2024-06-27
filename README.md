# Desafíos de Procesamiento de Texto

Este repositorio contiene soluciones y análisis para desafíos específicos de procesamiento de texto.

## Desafío 1: Vectorización y Similaridad de Documentos

El objetivo de este desafío es explorar la vectorización de documentos y medir la similaridad entre ellos. 

### Pasos y Análisis

1. **Vectorización de Documentos:**
   - Seleccionar 5 documentos al azar del conjunto de datos.
   - Utilizar técnicas de vectorización como TF-IDF o CountVectorizer para representar los documentos como vectores numéricos.

2. **Medición de Similaridad:**
   - Calcular la similaridad entre cada uno de los 5 documentos seleccionados y todos los demás documentos.
   - Identificar los 5 documentos más similares para cada uno y analizar si esta similaridad tiene sentido en función del contenido del texto y las etiquetas de clasificación asociadas.

3. **Análisis de Resultados:**
   - Evaluar si las medidas de similaridad reflejan correctamente las relaciones semánticas entre los documentos.
   - Comparar los resultados con las etiquetas de clasificación para verificar la coherencia.

### Archivos Incluidos

- `documento1.txt`, `documento2.txt`, ..., `documentoN.txt`: Ejemplos de documentos utilizados para el análisis.
- `vectorizacion.py`: Script para realizar la vectorización y cálculo de similaridad.
- `resultados_similaridad.csv`: Archivo CSV con los resultados de similaridad obtenidos.

Para más detalles sobre la implementación y ejecución de este desafío, consulta los scripts y archivos mencionados.

## Desafío 2: Custom Embeddings con Gensim

En este desafío, se explorará la creación de vectores personalizados utilizando Gensim basado en un e-book obtenido de Project Gutenberg.

### Objetivos

1. **Creación de Vectores con Gensim:**
   - Utilizar Gensim para entrenar vectores de palabras (embeddings) a partir del e-book proporcionado.
   - Aplicar técnicas como Word2Vec o FastText para generar representaciones vectoriales de términos del e-book.

2. **Análisis de Similitudes y Diferencias:**
   - Seleccionar términos de interés y explorar sus similitudes y diferencias en el espacio de embeddings.
   - Comparar cómo se relacionan semánticamente los términos según las distancias calculadas en el espacio vectorial.

3. **Visualización y Conclusiones:**
   - Graficar los embeddings para visualizar la distribución de los términos en un espacio dimensional reducido.
   - Extraer conclusiones sobre las relaciones semánticas entre los términos, identificando patrones de similitud y diferenciación.

### Datos

Los datos utilizados provienen del siguiente e-book de Project Gutenberg:

- **Título:** Introduction to the study of the history of language
- **Autores:** Herbert A. Strong, Willem Sijbrand Logeman, Benjamin Ide Wheeler
- **Fecha de Publicación:** 8 de enero de 2019
- **Idioma:** Inglés

### Archivos Incluidos

- `custom_embeddings.py`: Script para la creación y entrenamiento de embeddings personalizados con Gensim.
- `visualizaciones.ipynb`: Notebook Jupyter con visualizaciones de los embeddings y análisis de términos.
- `ebook_text.txt`: Texto del e-book utilizado para entrenar los embeddings.

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

