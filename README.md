# Detección de fraude con tarjetas de crédito

Proyecto de aula de Modelos y Simulación de Sistemas II, Universidad de Antioquia.

Integrantes: Kelly Julieth Arango Henao, Lisbeth Cataño Sepulveda

## De qué trata

Queremos predecir si una transacción con tarjeta es fraude o no, usando el
dataset de Kaggle "Credit Card Fraud Detection". Es un problema difícil porque
solo el 0,17 % de las transacciones son fraude.

## Qué hay en el repositorio

- `reporte/`: el informe del proyecto (Entregable I y II) en PDF
- `notebooks/`: el código con el análisis, los modelos y la reducción de
  dimensión; las gráficas y tablas generadas se pueden ver directamente en
  las salidas de cada notebook
- `data/`: aquí va el archivo de datos (ver abajo)

## Cómo correrlo

1. Descargar el dataset de Kaggle (https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
   y guardar `creditcard.csv` en la carpeta `data/`. El archivo no está incluido
   en este repositorio porque pesa más de lo que GitHub permite.
2. Instalar las librerías: `pip install -r requirements.txt`
3. Abrir los notebooks en orden:
   - `01_EDA.ipynb`: análisis exploratorio de los datos
   - `02_Modelos.ipynb`: preparación de los datos y entrenamiento de los cinco
     modelos (regresión logística, KNN, Random Forest, red neuronal y SVM)
   - `03_Reduccion_Dimension.ipynb`: análisis de variables y reducción de
     dimensión con PCA y UMAP

## Resultados principales

Random Forest fue el mejor modelo en validación y en prueba (AUPRC de 0,80 y
0,78 respectivamente). Los demás modelos (regresión logística, SVM, red
neuronal) quedaron con un desempeño similar entre sí, con intervalos de
confianza solapados. Más detalle en el reporte.

## Video de sustentación

...
