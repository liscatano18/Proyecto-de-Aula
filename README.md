# Detección de fraude con tarjetas de crédito

Proyecto aula de la asignatura Modelos y Simulación de Sistemas II de la Universidad de Antioquia.

**Integrantes:** Kelly Julieth Arango Henao, Lisbeth Cataño Sepulveda

## Descripción del proyecto

Este proyecto busca identificar transacciones fraudulentas con tarjetas de crédito mediante técnicas de aprendizaje automático (Machine Learning).

Para ello, se utiliza el conjunto de datos Credit Card Fraud Detection, disponible en Kaggle. Uno de los principales retos es el desbalance de clases, ya que aproximadamente el 0,17 % de las transacciones corresponden a fraudes.

Se realiza un análisis exploratorio de los datos, se entrenan y comparan diferentes modelos de clasificación y, finalmente, se evalúan técnicas de reducción de dimensionalidad.

## Estructura del repositorio

```text
├── data/
│   └── creditcard.csv
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Modelos.ipynb
│   └── 03_Reduccion_Dimension.ipynb
│
│
├── requirements.txt
└── README.md
```


- `data/:` contiene el conjunto de datos utilizado.

- `notebooks/:` incluye los notebooks del análisis exploratorio, entrenamiento de modelos y reducción de dimensionalidad.

- `requirements.txt:` incluye las dependencias necesarias para ejecutar el proyecto.

## Requisitos e instalación
    
1. Clonar el repositorio.

2. Descargar el dataset desde Kaggle - Credit Card Fraud Detection (https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

3. Guardar el archivo creditcard.csv dentro de la carpeta data/.  **Nota:** el dataset no se incluye en el repositorio debido a su tamaño.

4. Instalar las dependencias:

        `pip install -r requirements.txt`

5. Abrir y ejecutar los notebooks en el siguiente orden:

   | Notebook | Descripción |
   |---|---|
   | `01_EDA.ipynb` | Análisis exploratorio y comprensión del conjunto de datos. |
   | `02_Modelos.ipynb` | Preparación de los datos y entrenamiento de cinco modelos: Regresión Logística, KNN, Random Forest, Red Neuronal y SVM. |
   | `03_Reduccion_Dimension.ipynb` | Análisis de variables y aplicación de PCA y UMAP, comparando Random Forest y Regresión Logística con diferentes representaciones de los datos. |

## Resultados principales

- **Comparación de modelos:** Random Forest obtuvo el mejor resultado, con un AUPRC de 0,8034 en validación y 0,7833 en prueba.

- **Reducción con PCA:** Permitió trabajar con 23 componentes en lugar de 30, reduciendo la dimensionalidad en un 23,3 % y conservando un desempeño cercano al de las variables originales.

- **Reducción con UMAP:** consiguió una mayor reducción de dimensionalidad, pero también presentó una disminución importante en el desempeño predictivo.

En general, los resultados muestran que Random Forest fue el modelo con mejor desempeño y que PCA ofreció un mejor equilibrio entre la reducción de variables y la capacidad de detección de fraude.


