# Detección de fraude con tarjetas de crédito

Proyecto de aula de Modelos y Simulación de Sistemas II, Universidad de Antioquia.

Integrantes: Kelly Julieth Arango Henao, Lisbeth Cataño Sepulveda

## De qué trata

Queremos predecir si una transacción con tarjeta es fraude o no, usando el
dataset de Kaggle "Credit Card Fraud Detection". Es un problema difícil porque
solo el 0,17 % de las transacciones son fraude.

## Qué hay en el repositorio

- `reporte/`: el informe del proyecto (Entregable I y II) en PDF
- `notebooks/`: el código con el análisis, los modelos y la reducción de dimensión
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
     dimensión con PCA y UMAP, comparando los dos mejores modelos (Random
     Forest y regresión logística) con las variables originales, con PCA y
     con UMAP

## Resultados principales

Random Forest fue el mejor modelo en validación y en prueba (AUPRC de 0,80 y
0,78 respectivamente), seguido de cerca por la regresión logística, la SVM y
la red neuronal, con un desempeño similar entre sí.

Al reducir la dimensión, PCA mantuvo un desempeño muy cercano al de las
variables originales usando solo 23 de las 30 variables (23,3 % de
reducción). UMAP, en cambio, con solo 2 componentes (93,3 % de reducción),
perdió bastante desempeño, por lo que resultó más útil para visualización
que para mantener la capacidad de detección de fraude.

Más detalle en el reporte.



## Video de sustentación

...
