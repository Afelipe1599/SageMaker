# Tutorial de AWS

Acontinuación  se realiza el tutorial proupuesto en la [documentación de Amazon](https://docs.aws.amazon.com/es_es/sagemaker/latest/dg/ex1-preprocess-data-pull-data.html)

Este tutorial se compone de 4 partes:

1. Desgargar y tratar los datos:
Para este paso, se descargan los datos de un banco de datos y se guardan en el **BUCKET S3** de amazon.

1. Capacitar el modelo mediante el algoritmo xgboost:
En este paso se importa el algoritmo xgboots y se establecen los **hiperparámetros** del mismo, para concluir con este paso, se descargan los datos subidos en el paso anterior y se procede a entrenar el modelo

1. Implementar el modelo con la transformación por lotes:
La transformación por lotes consiste en utilizar un modelo entrenado con un conjunto de datos de entrada para obtener un resultado, este modelo de implementación se utiliza cuando no se necesita un **endpoint** persistente.


![batch-transform-v2.png](/Ejemplo01/batch-transform-v2.png)


1. Validar el modelo:
Para finalizar se descargan los resultados del trabajo de transformacion por lotes del bucket y se compara con los datos prueba para comprobar la eficiencia del modelo.


**BUCKET S3:** El bucket es el servicio de almacenamiento simple que ofrece amazon para que guardemos todo tipo de datos necesarios para la capacitacion de modelos, ademas de tambien guardar los resultados. 

**HIPERPARÁMETROS:** Parametros que recibe el algoritmo como profundidad, peso minimo de hijos, etc

**ENDPOINT:** Un endpoint o punto de enlace es una URL mediante la cual se conecta a un servicio de programación en AWS

[Notebook realizado](https://github.com/Afelipe1599/SageMaker/blob/main/Ejemplo01/tutoAWS.ipynb)