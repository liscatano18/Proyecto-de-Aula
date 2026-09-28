# Detección de fraude con tarjetas de crédito

Proyecto de aula – Modelos y Simulación de Sistemas II
Universidad de Antioquia

Integrantes: [Nombre 1], [Nombre 2], [Nombre 3]

## De qué trata el proyecto

Queremos predecir si una transacción con tarjeta de crédito es fraude o no,
usando el dataset público de Kaggle "Credit Card Fraud Detection". Es un
problema difícil porque solo el 0,17 % de las transacciones son fraude
(clases muy desbalanceadas).

## Qué hay en esta carpeta

```
reporte/        -> el informe del proyecto en PDF
notebooks/      -> el código, en orden numerado
data/           -> aquí va el archivo de datos (ver instrucciones abajo)
resultados/     -> gráficas que generan los notebooks
requirements.txt -> librerías necesarias para correr todo
```

## Cómo correrlo, paso a paso

### 1. Descargar el dataset

El archivo de datos no está en este repositorio porque pesa más de lo que
GitHub permite. Hay que descargarlo aparte:

1. Entrar a https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
2. Iniciar sesión y darle click a "Download"
3. Descomprimir el archivo si llega como .zip
4. Copiar el archivo `creditcard.csv` dentro de la carpeta `data/` de este
   repositorio (al clonar primeramente el proyecto)

Al final debe quedar así: `data/creditcard.csv`

### 2. Instalar lo necesario

Este proyecto usa Python. Si ya tienes Python instalado, abre una terminal
en esta carpeta y corre:

```
pip install -r requirements.txt
```

Si vas a correr los notebooks en Google Colab, no necesitas instalar nada:
Colab ya trae casi todo. Solo hay que subir el archivo `creditcard.csv` a
Colab o a Google Drive antes de correr el notebook (las instrucciones están
al inicio de cada notebook).

### 3. Correr los notebooks

Abrir la carpeta `notebooks/` y ejecutar los archivos en orden, de arriba
hacia abajo, celda por celda:

1. `01_EDA.ipynb` – análisis exploratorio de los datos
2. (los siguientes se agregan a medida que avanza el proyecto)

Cada notebook indica al inicio qué necesita antes de poder correr.

## Resultados principales

[Completar cuando se termine el análisis: cuántas transacciones, cuántos
fraudes, qué se encontró.]

## Video de sustentación

[Agregar el enlace aquí cuando esté listo.]
