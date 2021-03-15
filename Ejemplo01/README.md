# Tutorial de AWS

Acontinuación  se realiza el tutorial proupuesto en la [documentación de Amazon](https://docs.aws.amazon.com/es_es/sagemaker/latest/dg/ex1-preprocess-data-pull-data.html)

Este tutorial se compone de 4 partes:

1. Desgargar y tratar los datos:
Para este paso, se descargan los datos de un banco de datos y se guardan en el **BUCKET S3** de amazon.

1. Capacitar el modelo mediante el algoritmo xgboost:
En este paso se importa el algoritmo xgboots y se establecen los **hiperparámetros** del mismo, para concluir con este paso, se descargan los datos subidos en el paso anterior y se procede a entrenar el modelo

1. Implementar el modelo con la transformación por lotes:
La transformación por lotes consiste en utilizar un modelo entrenado con un conjunto de datos de entrada para obtener un resultado, este modelo de implementación se utiliza cuando no se necesita un endpoint persistente.

![](/https://docs.aws.amazon.com/es_es/sagemaker/latest/dg/images/batch-transform-v2.png)

1. Validar el modelo

**BUCKET S3:**  el bucket es el servicio de almacenamiento simple que ofrece amazon para que guardemos todo tipo de datos necesarios para la capacitacion de modelos, ademas de tambien guardar los resultados. 

**hiperparámetros:** Parametros que recibe el algoritmo como profundidad, peso minimo de hijos, etc