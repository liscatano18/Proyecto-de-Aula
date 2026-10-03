# Detección de fraude con tarjetas de crédito

Proyecto de aula – Modelos y Simulación de Sistemas II
Universidad de Antioquia

Integrantes: Kelly Julieth Arango Henao, [Nombre 2], [Nombre 3]

## De qué trata el proyecto

En este proyecto buscamos analizar y desarrollar un modelo que permita identificar si una transacción realizada con una tarjeta de crédito es normal o puede corresponder a un fraude.

Para esto estamos utilizando el conjunto de datos Credit Card Fraud Detection, disponible públicamente en Kaggle. El problema se plantea como un caso de aprendizaje supervisado, específicamente de clasificación binaria, porque el conjunto de datos ya tiene una variable que indica el resultado de cada transacción.

Las dos clases que se manejan son:

0: transacción normal.

1: transacción fraudulenta.

Uno de los principales problemas que encontramos desde el comienzo es que las transacciones fraudulentas son una cantidad muy pequeña en comparación con las transacciones normales. Esto genera un desbalance de clases que debemos tener en cuenta al momento de entrenar y evaluar los modelos.

Por esta razón, no vamos a basarnos únicamente en la exactitud del modelo. También tendremos en cuenta métricas como precision, recall, F1-score, ROC-AUC y AUPRC, ya que permiten analizar mejor qué tan bien se están identificando los casos de fraude.

## Conjunto de datos

Para el proyecto utilizamos el dataset Credit Card Fraud Detection, disponible en Kaggle.

El conjunto de datos contiene información relacionada con transacciones realizadas con tarjetas de crédito. Está compuesto por 31 columnas, de las cuales:

30 corresponden a variables que pueden ser utilizadas para hacer la predicción.

1 corresponde a la variable objetivo Class.

Entre las variables encontramos:

Time: representa el tiempo transcurrido desde la primera transacción.
V1 hasta V28: son variables numéricas anonimizadas. Estas variables fueron transformadas mediante PCA para proteger la información original de los usuarios.
Amount: corresponde al valor de la transacción.
Class: indica si la transacción es normal o fraudulenta.

El archivo utilizado para realizar el análisis es:

```
creditcard.csv
```
Por el tamaño del archivo, decidimos no incluirlo directamente dentro del repositorio de GitHub.

## Contenido del repositorio

```
reporte/ -> informe de la Entrega 1 en PDF
notebooks/ -> notebooks utilizados durante el desarrollo
data/ -> archivo creditcard.csv
resultados/ -> gráficas y resultados obtenidos
requirements.txt -> librerías necesarias para ejecutar el proyecto
README.md -> información e instrucciones del proyecto
```

### 1. Fuente de los datos y descargar el dataset

El archivo de datos no está en este repositorio porque pesa más de lo que
GitHub permite. Hay que descargarlo aparte:

1. Entrar a https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
2. Iniciar sesión y darle click a "Download"
3. Descomprimir el archivo si llega como .zip
4. Copiar el archivo `creditcard.csv` dentro de la carpeta `data/` de este
   repositorio (al clonar primeramente el proyecto)

Al final debe quedar así: `data/creditcard.csv`

### 2. Instalar lo necesario

El proyecto está desarrollado en Python. Para instalar las librerías necesarias se debe abrir una terminal en la carpeta principal del proyecto y ejecutar:

```
pip install -r requirements.txt
```

Si se utiliza Google Colab, la mayoría de estas librerías ya están disponibles. En este caso solamente es necesario cargar el archivo creditcard.csv y seguir las instrucciones que aparecen al inicio del notebook.

### 3. Ejecutar el notebook

Para esta primera entrega tenemos:

1. `01_EDA.ipynb` 

Este notebook corresponde al análisis exploratorio de los datos. En él revisamos principalmente:

La cantidad de registros y variables.
La información general de las columnas.
Los datos faltantes.
Los registros duplicados.
La distribución de las clases.
El comportamiento de los montos de las transacciones.
La distribución del tiempo.
La relación entre las variables y la clase objetivo.
La matriz de correlación.
Algunas gráficas para entender mejor los datos.

El notebook debe ejecutarse de arriba hacia abajo para poder reproducir los resultados.

## Resultados principales

En esta primera etapa nos enfocamos principalmente en entender los datos antes de comenzar con el entrenamiento de los modelos.

Uno de los resultados más importantes del análisis fue identificar el desbalance entre las transacciones normales y las fraudulentas. Esto es importante porque un modelo podría tener una exactitud aparentemente alta y aun así no detectar correctamente los casos de fraude.

También revisamos la calidad de los datos, incluyendo los valores faltantes y los registros duplicados, y analizamos algunas variables como Amount y Time para observar su comportamiento.

A partir de este análisis concluimos que el problema corresponde a un modelo de aprendizaje supervisado para clasificación binaria, donde buscamos diferenciar entre transacciones normales y fraudulentas.

Las gráficas generadas durante el análisis se guardan en la carpeta:

```
resultados/
```

## Video de sustentación

[Agregar el enlace aquí cuando esté listo.]
