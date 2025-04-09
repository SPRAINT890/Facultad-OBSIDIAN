
## Objetivo
- Estudiar algoritmos para lograr una comunicacion confiable y eficiente entre dos maquinas adyacentes

### Maquinas Adyacentes:
Conectadas por un canal de comunicaciones que actua conceptualmente como un alambre (los bits se entregan con exactitud en el mismo orden que fueron enviados).

- Estudiar las **limitaciones del canal** de comunicaciones que afectan la eficiencia de la transferencia de datos y deben ser tenidos en cuenta por los protocolos:
	- Errores
	- Tasa de datos finita
	- Retardo de propagacion (Diferencia de tiempo entre que se envia un bit y que se recibe)

## Diseño
- Servicios provistos a la capa de red
- Entramado (Framing)
- Control de Errores
- Control de flujo (Receptores lentos no sean saturados por emisores muy rapidos)
![[Pasted image 20250409193534.png]]

## Servicios
- Servicio no orientado a conexion sin confirmacion de recepcion (LAN)
- Servicio no orientado a conexion con confirmacion de recepcion (Canal Inestable)
- Servicio orientado a conexion con confirmacion de recepcion (Flujo de bits Confiable). Fases de establecimiento, transferencia y liberacion

Puede que en un mismo dispositivo haya varias capas de enlace de datos, un ejemplo son los ont de antel, que tiene uno distinto para la entrada wan a la entrada lan
![[Pasted image 20250409193859.png | 200]]

## Entramado
Solo ocurre en la capa 2
- Para cumplir con sus metas la capa de enlace de datos toma ***Paquetes*** de la capa de red y los encapsula en ***tramas*** para transmitirlos
- Cada trama contiene un encabezado, un campo de carga util (Payload) para almacenar el paquete y un terminador.
- El manejo de las tramas es la tarea principal de la capa de enlace de datos
![[Pasted image 20250409200514.png |450]]

#### Metodos de Entramado

##### Conteo de caracteres
- Propenso a fallos por la capa fisica
![[Pasted image 20250409200542.png | 450]]

##### Relleno de Caracteres
Trama delimitada por banderas (Bytess Especiales)

![[Pasted image 20250409200600.png | 450]]

##### Relleno de Bits
![[Pasted image 20250409200623.png]]

##### Violaciones de codificacion de la capa fisica
![[Pasted image 20250409200643.png | 450]]
