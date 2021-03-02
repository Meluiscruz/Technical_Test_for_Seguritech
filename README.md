# Desarrollo de la prueba técnica para Seguritech

## Metricas del proyecto

![](https://img.shields.io/github/stars/Meluiscruz/Technical_Test_for_Seguritech.svg) ![](https://img.shields.io/github/forks/Meluiscruz/Technical_Test_for_Seguritech.svg)
![](https://img.shields.io/github/issues/Meluiscruz/Technical_Test_for_Seguritech.svg)![](https://img.shields.io/github/tag/Meluiscruz/Technical_Test_for_Seguritech.svg)

## Interpretación de los requerimientos

Los requerimientos listados en [problemStatement.pdf](https://github.com/Meluiscruz/Technical_Test_for_Seguritech/blob/master/source_code.ipynb "source_code.ipynb")

## Estrategia de resolución

La estrategia se puede resumir en 3 etapas consecutivas y ordenadas:

1. Acondicionamiento y carga del dataset.
2. Creación de RDDs y DataFrames de manera deductiva.
3. Presentación de resultados.

Estas etapas están subdivididas en 9 secciones, mismas que están comentadas en el archivo [source_code.ipynb](https://github.com/Meluiscruz/Technical_Test_for_Seguritech/blob/master/source_code.ipynb "source_code.ipynb"):

1. Definimos la cabecera del proyecto.
2. Declaramos la ruta del dataset (que es una copia destilada del archivo original).
3. Leemos el archivo para crear el primer cleanMolochDataRDD.
4. Creamos un DF (DF_Moloch) a partir del RDD del paso anterior.
5. Creamos un RDD (RDD_OnlyJsonData) que contenga solo las strings en formato JSON
6. Creamos el DF (onlyJsonData_DF) a partir del RDD de strings en formato JSON.
7. Declaramos el DF srcIP_DF a partir del DF onlyJsonData_DF.
8. Declaramos el DF groupByProtocol_DF a partir del DF onlyJsonData_DF.
9. Hacemos un filtro del DF por jerarquía de protocolos.

## Tabla de contenido

- [/files](https://github.com/Meluiscruz/Intro_a_Spark/tree/master/files "files"): Directorio que contiene los datasets del proyecto.
- [/Images](https://github.com/Meluiscruz/Intro_a_Spark/tree/master/Images "Images"): Directorio de imagenes miscelanias, no relevante.
- [/Notebooks](https://github.com/Meluiscruz/Intro_a_Spark/tree/master/Notebooks "Notebooks"): Es donde habitan los Jupyter Notebooks y archivos html del proyecto.
  - [/Notebooks/Instrucciones_de_configuracion_y_uso](https://github.com/Meluiscruz/Intro_a_Spark/tree/master/Notebooks/Instrucciones_de_configuracion_y_uso "Instrucciones de config"): El archivo main.html indexa las notas de Cornell relativas a los modulos 1, 2 y 3 del curso. 
 
- [/codeExample.py](https://github.com/Meluiscruz/Intro_a_Spark/blob/master/codeExample.py "codeExample.py"): Es un ejemplo de script de pySpark que tiene dos propositos; comprobar la instalación del framework y demostrar lo impractico que es trabajar con scripts de pyspark en ambientes productivos. 

- [/data.csv](https://github.com/Meluiscruz/Intro_a_Spark/blob/master/data.csv "data.csv"): Dataset de prueba para la verificaci{on de la instalación del framework. 

## ¿Qué está pendiente por desarrollar?

- La versión en inglés del Jupyter Notebook principal.

- Un script mejor definido sobre la limpieza del archivo csv original.

- La versión en inglés del README.md.

## Información técnica

Este proyecto fue elaborado con el siguiente stack:

- Jupyter Notebook / ipython 7.12.0
- Python 3.7.9
- Spark v2.4.7
- Ubuntu 20.04.2 LTS
