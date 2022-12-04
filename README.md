## Dataset a usar
El dataset fue extraido por la cátedra para distintas canciones, y se encuentre [acá](https://drive.google.com/drive/folders/1-S0MrftIbCRalfL876-p2hyMkrX52TKM).

El target a predecir es el género de la canción en la columna genre.

La métrica de validación es top-2 accuracy.

## PARTE I
Se realizaron 6 visualizaciones explicando el target, dos bar plots, dos box plots, un violin plot y un heatmap. 

## PARTE II (Baseline.ipynb)
Se construyó un modelo muy sencillo para saber qué es lo peor que podemos hacer, en general esta es una tarea muy importante que queremos que repitan en sus proyectos de machine learning.

+ Nos sirve para saber si estamos usando bien los modelos más complejos, si su score nos da peor al baseline probablemente se deba a un error de código.
+ Nos sirve para rápidamente saber que tan complejo es un problema.
+ Los modelos simples son fáciles de entender.

Con el baseline obtuvimos un score de validación de: 0.5075757575757576

Se utilizaton todas las columnas del dataset (exceptuando columnas que no tenga sentido usar para predecir) con algún encoding donde sea necesario para entrenar una regresión logística, utilizando búsqueda de hiperparametros y garantizando la reproducibilidad de los resultados cuando el notebook corriera varias veces. 
Contestando las preguntas:
+ ¿Cuál es el mejor score de validación obtenido? (¿Cómo conviene obtener el dataset para validar?)
+ Al predecir con este modelo para test, ¿Cúal es el score obtenido? (guardar el csv con predicciones para entregarlo después)
+ ¿Qué features son los más importantes para predecir con el mejor modelo? Graficar.

## PARTE III (RandomForest.ipynb y XGBoost.ipynb): 
Se entrenaron 2 modelos, RandomForest y XGBoost, con búsqueda de hiperparametros. Los modelos deben cumplen las siguientes condiciones:

+ Se uso  top-2 accuracy como métrica de validación.
+ Son reproducibles (correr el notebook varias veces no afecta al resultado).
+ Tienen un score en validación superior a 0,3.
+ Para el feature engineering se utilizó imputación de nulos, mean encoding y one hot encoding al menos una vez cada uno.
+ Se utilizaron al menos 40 features (contando cómo features columnas con números, pueden venir varios de la misma variable).
+ Se utilizó CountVectorizer o TfIdfVectorizer para algunos features.

Se obtuvo un mejor resultado con RandomForest, el score de test fue de 0.5111712931618145



  


