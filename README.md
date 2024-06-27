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

## Cómo Ejecutar

1. Clona este repositorio:
