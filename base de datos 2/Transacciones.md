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


| Atomicidad                                                                                                       | Conservacion de la Consistencia                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Una transaccion es una unidad atomica de procesamiento; o se ejecuta en su totalidad o no se ejecuta en absoluto | Una transacción esta conservando la consistencia si su ejecución completa lleva la base de datos de un estado consistente a otro<br>(No pue) |

