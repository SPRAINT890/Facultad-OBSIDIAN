## Clasificacion de DBMS
Un criterio que permite clasificar los sistemas de base de datos es el numero de usuarios que lo pueden utilizar al mismo tiempo


| Monousuario                                        | Multiusuarios                                                 |
| -------------------------------------------------- | ------------------------------------------------------------- |
| Si y solo si lo puede utilizar un usuario a la vez | Si varios usuarios pueden utilizar el sistema simultaneamente |
## Ejemplo de transaccion
![[Pasted image 20240905185404.png]]


| T1           | T2        |
| ------------ | --------- |
| X=9          | X=9       |
| X=8          | X=11      |
| write(X, 8)  | write(11) |
| Y=10         |           |
| Y=11         |           |
| write(Y, 11) |           |
## Ejemplo de Actualización perdida

X = 80
N = 5
M = 4

![[Pasted image 20240905185658.png]]

## Ejemplo de Actualización temporal

![[Pasted image 20240905190404.png]]

## Ejemplo de Suma Incorrecta

![[Pasted image 20240905190548.png]]

## ¿Que es una Transaccion?
- Una transaccion es una unidad atomica de trabajo que se completa en su totalidad o no se lleva a cabo en absoluto
- A los efectos de la recuperación, el sistema debe de hacer seguimiento de cuándo se inicia, termina, confirma y aborta una transacción

## Necesita tener Control de concurrencia
Control de concurrencia se define como la ***coordinación*** de los procesos ***concurrentes*** que ***operan*** sobre ***datos*** ***compartidos*** y que podrían ***interferir*** entre ellos.

## Propiedades deseables ACID


|                                                    Atomicidad                                                    |                                                                      Conservacion de la Consistencia                                                                       |                                                                                         Aislamiento (Isolated)                                                                                         |                                                                      Durabilidad                                                                       |
| :--------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------: |
| Una transaccion es una unidad atomica de procesamiento; o se ejecuta en su totalidad o no se ejecuta en absoluto | Una transacción esta conservando la consistencia si su ejecución completa lleva la base de datos de un estado consistente a otro<br>(No se rompe nada cuando ejecuto algo) | Una transacción debe aparecer como si estuviera ejecutándose de forma aislada a las demás. La ejecución de una transacción no debe interferir con la ejecución de ninguna otra transacción simultánea. | Los cambios aplicados a la base de datos por una transacción confirmada deben persistirse. Estos cambios no deben perderse a consecuencia de un fallo. |

## Operaciones de las Historias


| Read_Item $r_i$ (x)                | Write_Item $w_i$ (x)                   | Commit $c_i$                   | Abort $a_i$                          |
| ---------------------------------- | -------------------------------------- | ------------------------------ | ------------------------------------ |
| La transacción i lee un elemento X | La transacción i escribe un elemento X | La transacción i es confirmada | La transacción i aborta la ejecución |

## Rollback
- Es una acción que se dispara ante un abort de una transacción
- Lleva la base de datos a su estado anterior

## ¿Que es una Historia?
- Cuando las transacciones se están ejecutando concurrentemente en modo interpolado, el orden de ejecución de las distintas transacciones se conoce como planificación o historia
- La historia es una ordenación de todas las operaciones que intervienen en las transacciones
- Las operaciones deben aparecer en el mismo orden que en cada una de las transacciones

### Ejemplo de historia
$T_1 = r_1 X$, $w_1 X$, $r_1 Y$, $w_1 Y$, $c_1$
$T_3 = r_3A$, $r_3X$, $r_3Y$, $c_3$

![[Screenshot_20240905_194117_Samsung Notes.jpg]]
La de arriba es entrelazada y la de abajo es serial

## Operaciones en conflicto
Se dice que dos operaciones están en conflicto si satisfacen las siguientes tres condiciones:
- Pertenecen a diferentes transacciones
- Acceden al mismo elemento X
- Por lo menos una de las operaciones es un write ($w_i$)
![[tempFileForShare_20240905-200930.jpg]]

## Una historia es completa cuando
Una historia completa es aquella que tiene todas las operaciones de las transacciones involucradas y las operaciones en conflicto aparecen en el mismo orden

## Historia seriales y entrelazadas
##### Las operaciones de las transacciones no están intercaladas
- No hay concurrencia 
- Los datos siempre están correctos
##### Si las historias están entrelazadas puede suceder que:
- Los datos queden incorrectos y no puedan ser corregidos 
- Si una transacción aborta, que otra también tenga que abortar

## Historia Serializables
##### Necesitamos lo mejor de los dos mundos
- Historias entrelazadas 
- Pero que funcionen como seriales

Una historia serializable es aquella que es equivalente a una historia serial con las mismas transacciones

## Historias Equivalentes
##### Intuitiva 
- Dos historias son equivalentes si dejan la base de datos en el mismo estado 
- Esta idea es fácil de comprender, pero difícil de garantizar en la práctica. Puede darse por casualidad.
##### Por conflicto 
- Tienen todas las operaciones en conflicto en el mismo orden

## Grafo de Serialidad
1. Poner un nodo por cada transacción de la historia
2. Crear un arco de $T_j$ a $T_i$ si se cumple alguna de las siguientes:
	- Si  $r_i$ (X) esta despues de $w_j$ (X)
	- Si $w_i$ (X) esta despues de $r_j$ (X)
	- Si $w_i$ (X) esta despues de $w_j$ (X)
3. Si se genera un ciclo la historia no es serializable

##### Serializable
![[Pasted image 20240905202314.png|600]]

##### No Serializable
![[Pasted image 20240905202342.png | 600]]



## Historias recuperables
- Una vez confirmada una transacción T, nunca será necesario anularla (rollback)
- Las historias que cumplen con este criterio se denominan recuperables 
	- Las que no lo cumplen (irrecuperables), no las debemos permitir
- Una historia S es recuperable, si ninguna transacción T en S se confirma hasta que todas las transacciones T’ que han escrito un elemento que T lee se han confirmado
Los commits tienen que estar en el mismo orden que los writes en conflicto

### Ejemplo
H = r1 (X), w1 (X), r2 (X), r1 (Y), w2 (X), c2 , a1
#### No es Recuperable porque:
- T2 lee el elemento X de T1 
- Se confirma T2 antes que T1 
- T1 se cancela después de que T2 se confirma 
- El valor de X que lee T2 ya no es válido 
- T2 debería cancelarse después de ser confirmada

## Evita Anulación en Cascada (Aborto en cascada)
- En una historia recuperable, ninguna transacción confirmada debe ser anulada 
- Fenómeno de la Anulación en Cascada 
	- Una transacción no confirmada tiene que ser anulada porque lee un elemento de una transacción que falló 
- Las anulaciones en cascada consumen mucho tiempo, por lo que es conveniente evitarlas

- Una historia Evita Anulaciones en Cascada (EAC), si cada transacción de la historia solo lee elementos escritos por transacciones confirmadas 
- Por lo tanto, los commits tienen que estar antes de los reads de las transacciones siguientes
Ninguna transaccion puede leer si no esta confirmada

## Historia Estrictas
- En una historia Estricta las transacciones no pueden leer ni escribir un elemento X hasta que la última transacción que escribió X se confirme (o cancele) 
- Las historias estrictas simplifican el proceso de recuperación 
	- Deshacer una operación write (X) de una transacción cancelada es simplemente recuperar la imagen anterior del elemento X 
	- Siempre funciona para historias estrictas, pero puede no funcionar para historias recuperables o EAC
No podes leer ni escribir si la transacción esta confirmada
