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


#### Dendrograma
Un **dendrograma** es un **diagrama en forma de árbol** que se utiliza para representar cómo se agrupan los elementos en un proceso de **clustering jerárquico** sin la necesidad de elegir un numero de clusters, existe dos formas Bottom-Up y Top-Down.

##### Bottom-Up
Empieza tomando cada fila como un cluster y los va agrupando segun su distancia, hasta formar un cluster general
Ventajas:
- Simple y ampliamente usado. 
- No necesitas definir el número de clusters desde el inicio

desventajas:
- Costoso computacionalmente para grandes datasets.
- No permite deshacer fusiones (es _greedy_).
##### Top-Down
Parte de un cluster general, y lo va dividiendo segun la distancia hasta llegar a un cluster por fila
Ventajas:
- Puede producir particiones más globalmente óptimas si se implementa bien. 
- Útil si los datos tienen una estructura jerárquica clara desde el inicio.

Desventajas:
- Más difícil de implementar correctamente.
- Menos común en bibliotecas estándar.
- Requiere criterios más sofisticados para dividir los clusters.

#### ¿por que es necesario utilizar un conjunto de validacion y uno de testeo?

Supongamos que tienes un dataset completo. Se suele dividir en tres partes:

| Conjunto                    | ¿Para qué se usa?                                              |
| --------------------------- | -------------------------------------------------------------- |
| **Entrenamiento** (train)   | Para entrenar el modelo (ajustar sus parámetros)               |
| **Validación** (validation) | Para ajustar hiperparámetros y elegir el mejor modelo          |
| **Prueba/Testeo** (test)    | Para evaluar el rendimiento final, **como si fuera un examen** |
###### **Entrenamiento**
- Aquí el modelo aprende directamente de los datos.
- Se ajustan los pesos, coeficientes, etc.

###### **Validación**
- Aquí el modelo **no aprende**, solo se evalúa.
- Se usa para: 
    - Comparar diferentes arquitecturas o modelos.
    - Elegir valores de **hiperparámetros** (número de árboles, regularización, etc.).
    - Evitar sobreajuste al conjunto de entrenamiento.
> Sin validación, puedes terminar **eligiendo un modelo que funciona bien solo en los datos que vio**.

###### **Testeo (prueba final)**
- Este conjunto **no debe usarse hasta el final**.
- Se reserva para una **evaluación honesta del modelo final**.
- Simula el comportamiento del modelo con **datos nuevos del mundo real**.
> Si pruebas muchas veces en el set de test, **empiezas a sobreajustar inconscientemente a él**, y deja de ser una medición confiable.

#### ¿Que tipo de enlace hay en la clasificacion jerarquica?
###### **Single Linkage** (Enlace simple)
- Usa la **distancia más corta** entre cualquier par de puntos de dos clusters.
🟢 detecta estructuras largas como cadenas.  
🔴 **efecto cadena** (puede unir clusters mal conectados por un punto).

###### **Complete Linkage** (Enlace completo)
- Usa la **distancia más lejana** entre puntos de dos clusters.
🟢 produce clusters compactos.  
🔴 sensible a _outliers_.

###### **Average Linkage** (Enlace promedio)
- Usa el **promedio de todas las distancias** entre puntos de ambos clusters.
🟢 Buen equilibrio entre single y complete.  
🔴 Puede ser más costoso computacionalmente.

###### **Centroid Linkage** (Enlace de centroide)

- Usa la **distancia entre los centroides** (medias) de los clusters.
🟢 Intuitivo y útil cuando los clusters tienen forma esférica.  
🔴 Puede producir resultados **no jerárquicos** (los clusters pueden separarse después de unirse, lo cual es problemático).

###### **Ward Linkage** (Enlace de Ward)
- Busca **minimizar el aumento de la varianza intra-cluster** al fusionar dos clusters.
🟢 Muy bueno para crear clusters **compactos y bien separados**.  
🔴 Supone que los datos son numéricos y usan distancia euclidiana.