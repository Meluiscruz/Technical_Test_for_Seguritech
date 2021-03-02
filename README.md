# Desarrollo de la prueba técnica para Seguritech

## Metricas del proyecto

![](https://img.shields.io/github/stars/Meluiscruz/Technical_Test_for_Seguritech.svg) ![](https://img.shields.io/github/forks/Meluiscruz/Technical_Test_for_Seguritech.svg)
![](https://img.shields.io/github/issues/Meluiscruz/Technical_Test_for_Seguritech.svg)![](https://img.shields.io/github/tag/Meluiscruz/Technical_Test_for_Seguritech.svg)

## Interpretación de los requerimientos

Los requerimientos listados en [problemStatement.pdf](https://github.com/Meluiscruz/Technical_Test_for_Seguritech/blob/master/problemStatement.pdf "problemStatement.pdf") sugieren un acercamiento deductivo y serializado. En otras palabras, no se puede avanzar al siguiente objetivo sin antes haber reuelto los anteriores.

El primer y segundo requerimiento expresan que el dataset debe ser acondicionado para poder desplegar los metadatos propios de un string en formato JSON.

El tercer requerimiento consiste en presentar dos medidas de estadística descriptiva (media y desviación estandar) de tres metadatos, esto es para todas las columnas.

Por último, se requiere presentar las mismas medidas para los mismos metadatos, solo que ahora hay una condición de filtrado implicita, que obliga al desarrollador a tratar con las expresiones más profundas y elementales del esquema JSON.

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

- [/data_sources](https://github.com/Meluiscruz/Technical_Test_for_Seguritech/tree/master/data_sources "/data_sources"): Directorio que contiene el archivo de trabajo (dataSyntheticMoloch.csv). Este dierectorio tambien contiene un cuaderno de pruebas para la limpieza del dataset (cleaning_dataset.ipynb) y una copia del dataset original (clean_dataSyntheticMoloch.csv).

- [problemStatement.pdf](https://github.com/Meluiscruz/Technical_Test_for_Seguritech/blob/master/problemStatement.pdf "problemStatement.pdf"): Archivo pdf donde se especifican los requerimientos del proyecto.

- [source_code.ipynb](https://github.com/Meluiscruz/Technical_Test_for_Seguritech/blob/master/source_code.ipynb "source_code.ipynb"): Es el cuaderno (Jupyter Notebook) donde está el desarrollo de la prueba técnica.

## ¿Qué está pendiente por desarrollar?

- La versión en inglés del Jupyter Notebook principal.

- Un script/cuaderno mejor definido para la automatización de la limpieza del archivo csv original.

- La versión en inglés del README.md.

## Información técnica

Este proyecto fue elaborado con el siguiente stack:

- Jupyter Notebook / ipython 7.12.0
- Python 3.7.9
- Spark v2.4.7
- Ubuntu 20.04.2 LTS
