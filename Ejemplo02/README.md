# Ejemplo con la herramienta Experimentos

Para este ejercicio se utilizó la herramienta [AutoPilot](https://aws.amazon.com/es/sagemaker/autopilot/) de Amazon SageMaker la cual crea, entrena y ajusta de forma automatica modelos de [ML](https://cleverdata.io/que-es-machine-learning-big-data/#:~:text=Machine%20Learning%20es%20una%20disciplina,complejos%20en%20millones%20de%20datos.) en función de sus datos.

Su funcionamiento consiste en proporcionar un conjunto de datos y seleccionar un objetivo(Para este caso en especifico es la calidad del vino), Autopilot construira multiples modelos midiendo su precisión.Al final de su busquedad, Autopilot ofrecera el mejor modelo encontrado para su despliegue.

![product-page-diagram_SageMaker_Auto-Pilot_dk-bg@2x.e2d27caf8ec3224f1498d904aee630f61c847359.png](/Ejemplo02/product-page-diagram_SageMaker_Auto-Pilot_dk-bg@2x.e2d27caf8ec3224f1498d904aee630f61c847359.png)

## Ejemplo Vino

Para este ejemplo, primero descargamos un dataset y lo dividimos para posteriormente subirlo al bucket de S3, este paso es muy importante pues Autopilot trabaja con datos subidos al bucket de Amazon.

[Preparando los datos](https://github.com/Afelipe1599/SageMaker/blob/main/Ejemplo02/prepare_data.ipynb)

posterior a la preparación de los datos procedemos a crear el experimento, para esto nos vamos a la categoria de Components and registries y seleccionamos Experiments and trials.

![Captura01.PNG]({{site.baseurl}}/Ejemplo02/Captura01.PNG)

Una vez ahi seleccionamos crear experimento y le proporcionaremos los datos para crear el experimento:

1. Nombre del experimento.
1. Bucket de S3 en donde estan los datos.
1. Fichero de entrenamiento.
1. Columna objetivo.
1. Bucket donde iran todos los artefactos y resultados.
1. Nombre del fichero donde van a ir los artefactos y resultados.

![Captura02.PNG]({{site.baseurl}}/Ejemplo02/Captura02.PNG)

![Captura03.PNG]({{site.baseurl}}/Ejemplo02/Captura03.PNG)

Posterior a crear el experimento y despues de unos minutos, Autopilot generara el mejor modelo posible listo para desplegar.

![Captura04.PNG]({{site.baseurl}}/Ejemplo02/Captura04.PNG)

Para desplegarlo creamos un endpoint con su nomenclatura correspondiente y ya estaria listo para ser testeado.

![Captura05.PNG]({{site.baseurl}}/Ejemplo02/Captura05.PNG)

Por ultimo y para ser testeado se utilizo creo una funcion infer como se muestra en el siguiente notebook

[Inferencia de datos](https://github.com/Afelipe1599/SageMaker/blob/main/Ejemplo02/inference.ipynb)




