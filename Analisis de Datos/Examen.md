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
pca, analisis no supervisado
1- Varianza expl total
2- Relacion entre variables, si son cercanos a 90 son independientes
3- importancia de cada variable en los componentes de cada variables
	- vector horizontal, no aporta al componente principal vertical
	- vector vertical, no aporta al componente principal horizontal
4- Tamaño de la flecha
5- Outliers
6- Tendencia
7- Datos promedio 

#### K-Means (No supervisado)
- Eleccion de los centroides, pueden ser aleatorios,  seleccion, forzado.
- Se asignan todos los puntos al centroide mas cercano, hablando de la distancia, de cada punto a cada centroide, y se asigna ese punto al cluster mas cercano, hay distintas medidas de distancias
- cada punto al cluster mas cercano, se recalcula los centroides, cuando el centroide se mueve hay que reasignar todos los puntos devuelta, fijandose los puntos del centroide, y asi sucesivamente hasta que los centroides se dejen de mover, significa que no se estan reasignando.

#### Pam (No supervisado)
se utilizan medoides, los cuales son puntos reales
se asignan los medoides de forma aleatoria, agrupado o forzoso,
se asigna un punto al medoide
se calcula el costo total de cambiar el medoide actual por cada punto del cluster.
se vuelve a reclasificar los puntos, se vuelve a comparar las distancias entre los puntos y se selecciona como medoide al menor, asi hasta que se deje de mover los medoides o hasta que terminen los ciclos

#### Arbol de decision Entropia y ganancia
Entropia medida de desorden, cuando es 0 no hay desorden y cuando es 1 es el maximo

ganancia, mayor orden de la variable objetivo,

Utilizan la entropia para calcular la ganancia de cada columna, la col con mayor gan, significa que tiene mayor orden a la hora de seleccionar el atributo raiz, segun la opcion que haya en esa columna. si la entropia es cero, todo dato que vaya a esa columna va a ser clasificado en una hoja, si no es cero es utilizado en otra columna, viendo los datos con mayor ganancia. repitiendo asi el proceso hasta que formar el arbol.

#### Bayesiano
Clasificador probabilistico, siendo que el que tenga mayor probabilidad, se elige como clase.


##### Supervisado y no sup
Los supervisados no predicen si no que muestran patrones de comportamiento mientras que no supervisado predicen.



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
