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
