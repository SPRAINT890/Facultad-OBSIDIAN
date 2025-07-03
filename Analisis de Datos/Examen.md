2h de examen
6 preguntas de desarrollo
20 preguntas multiple opcion
operaciones con tablas
traer calculadora
decision de variables

arbol no normalizacion
k means normalizacion

- pca
- aprendizaje sup y no sup
- preguntas conceptuales, teorica, como hacer un modelo, que inconsistencia buscaria, o como lo buscaria.
- que implica un analisis exploratorio
- exploracion de datos, visualizacion
- diferencia entra varianza y desviacion estandar
- tendencia central (media, promedio, moda)
- como mejorar un grafico en parte a visualizacion
- que tips vimos (5 buenas practicas)
- histograma, boxplot, de grafico, heatmap, nube de palabras (para que sirven, cuando usarias uno en vez de otro)
- clasificacion, supervisado, regresion, etc
- pam
## Grafico de Codos
Se puede usar para pca o para clustering, en pc se grafica abajo el componente principal, y a la derecha la varianza aplicada, se utiliza por que en pca se quiere reducir el volumen, para eso necesito una buena varianza aplicada, la suma de todos los componentes da 100% la cantidad de componentes maximos es la cantidad de variables del dataset.

las filas son combinaciones lineales de,

el grafico determina con cuantos pca me quedo, para hacer el analizis.


Para clustering
Inercia (SSE) por Clusters, a medida que va aumentando los clusters, la inercia va disminuyendo,
el calculo del sse es la distancia media de cada punto al centroide del cluster,

## Codo
un codo es un punto en el cual a partir de agregar un valor mas, no cambia mucho el valor total.

## Indice de Silueta
Objetivo, Medir que tan similar es la distancia entre puntos de un cluster en comparacion con los puntos de otro cluster


Intra (a): distancia promedio entre un cluster
(b): distancia entre ese punto y los puntos del cluster mas cercano, se calcula la distancia promedio de un cluster y el de otro, tomando el valor mas cercano

que tan separados estan los clusters

1 significa que todos los valores del mismo cluster esten en el mismo punto de medicion
0 
-1 solapacion de clusters

para llegar a 1, a tiene que ser cero
Indice = 1 si a = 0
indice = -1 si b = 0


## Correccion del primer parcial
#### Matriz de confusion


|               | Pos Real | Neg Real |
| ------------- | -------- | -------- |
| Pos Predichos | 155      | 35       |
| Neg Predicho  | 10       | 50       |


| VP     | FP     |
| ------ | ------ |
| **FN** | **VN** |
Accuracy (FP)
que se acierta mas, los positivos o los negativos
tipo de desbalance 


Recall sirve para ver que tan errado esta en los positivos, que en los negativos
Precision 
#### Como se evalua un metodos de clasificacion y como se utilizan
La mismas que la matriz de confusion en clasificacion.

desde que se crea el modelo, se crea una parte para validacion o de testeo, y se compara con el valor predicho con el real.

en regresion, se evalua que tan cerca esta el predicho del real.
MCE (Penaliza los outliners), MAE (Valor absoluto), MRC(Penaliza los outliners al cuadrado), MAPE()

#### Biplot
1- Varianza expl total
2- Relacion entre variables, si son cercanos a 90 son independientes
3- 
4-
5-
6-

##### Analizis de covarianza
Para ver dependencias
##### Matriz de confusion de varias columnas
precision fila
recall columna

Para A

|     | A   | B   | C   |
| --- | --- | --- | --- |
| A   | VP  | FP  | FP  |
| B   | FN  |     |     |
| C   | FN  |     |     |

Para B

|     | A   | B   | C   |
| --- | --- | --- | --- |
| A   |     | FN  |     |
| B   | FP  | VP  | FP  |
| C   |     | FN  |     |

Para C

|     | A   | B   | C   |
| --- | --- | --- | --- |
| A   |     |     | FN  |
| B   |     |     | FN  |
| C   | FP  | FP  | VP  |
