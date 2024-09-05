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
