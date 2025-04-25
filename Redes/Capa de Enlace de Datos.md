
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


## Control de Errores
¿Cómo asegurar que todas las tramas se entreguen en el orden apropiado a la capa de red del destino?

La manera normal de asegurar la entrega confiable de datos es proporcionar retroalimentación al emisor sobre lo que está ocurriendo al otro lado de la línea.

- Confirmaciones de recepción (positiva o negativa (ACK)).
- Temporizadores.
- Números de secuencia en las tramas.

![[Pasted image 20250409201512.png | 450]]
![[Pasted image 20250409201531.png | 450]]
Por que hay casos de error, se implementaron los temporizadores por protocolos

![[Pasted image 20250409201721.png | 450]]

#### Otro Caso de error
![[Pasted image 20250409201830.png | 450]]
Por eso se crearon los Numeros de Secuencia

![[Pasted image 20250409201930.png | 450]]


#### Control de Flujos
Se trata de evitar que el transmisor envíe tramas a una velocidad más alta de la que el receptor puede aceptarlas.

- Control de flujo basado en retroalimentación.
- Control de flujo basado en la tasa de transmisión.

#### Deteccion y correccion de errores
Existen dos estrategias básicas para manejar los errores.

Una es incluir suficiente información redundante para que el receptor pueda deducir cuáles debieron ser los datos transmitidos.

La otra estrategia es incluir sólo suficiente redundancia para permitir que el receptor sepa que ha ocurrido un error y entonces solicite una retransmisión.

- Códigos de corrección de errores (FEC) -> permiten corregir los errores en el receptor.
- Códigos de detección de errores.

##### Codigo de correccion de errores
- Trama de M bits de datos
- Con R bits redundantes (de verificacion)
- N = M + R
- Palabras codificadas de N bits

##### Deteccion de errores usando paridad
- Se añade un bit de pariedad al final de la palabra de forma que el número total de unos, incluido el bit de paridad sea par (paridad par) o impar (paridad impar).

- Paridad par:                1011000  1
- Paridad impar:  1101011  0
- Este código tiene una distancia de hamming igual a 2, así que es capaz de detectar errores en 1 bit.

Ejemplos (4 bits datos + 1 bit paridad)

1) 1100_

2) 1001_

3) 0111_

4) 1100_
![[Pasted image 20250409203715.png | 450]]

##### Correcion de errores con el Codigo de Hamming
- 10001001
- 10110001
- 00111000 Suma
- Distancia de Hamming d=3

Cantidad de posiciones de bits en la que difieren dos palabras codificadas.
Se requieren 3 errores de un bit para convertir una palabra en la otra.

- Palabras válidas de un código

  0000000000  0000011111

  1111100000  1111111111

- Distancia del código d=5
- Mínima distancia entre dos palabras válidas del código.
- Para detectar d errores, necesitamos un código con distancia d+1
- Para detectar y corregir d errores, necesitamos un código con distancia 2d+1

- M bits del mensaje
- R bits de Pariedad (Bits extra)
- Objetivo: corregir errores simples
- 2^m mensajes legales o válidos
- n+1 palabras por mensajes

- $(n+1)2^m=<2^n$

- $m+r+1=<2^r$. Límite inferior

Ejemplo: $m=7$ => $r=4$

- La palabra codificada se numera comenzando por el 1 a la izquierda.

- Los bits en las posiciones que son potencias de 2 (1,2,4,8,…) son bits de verificación; el resto (3,5,6,7, …) son datos.

- Los bits de verificación fuerzan la paridad de un grupo de bits (incluido él para ser par o impar).Un bit puede estar incluido en varios cálculos de paridad.


#### Ejemplo
La maquina quiere mandar este mensaje

##### Inicio
Tx -> M = 1 0 1 1 0 1 0

![[Pasted image 20250411200805.png]]

|             | R1 (Pos 1) | R2 (Pos 2) | R3 (Pos 4) | R4 (Pos 8) |
| ----------- | ---------- | ---------- | ---------- | ---------- |
| b1 (Pos 3)  | 1          | 1          | 0          | 0          |
| b2 (Pos 5)  | 1          | 0          | 1          | 0          |
| b3 (Pos 6)  | 0          | 1          | 1          | 0          |
| b4 (Pos 7)  | 1          | 1          | 1          | 0          |
| b5 (Pos 9)  | 1          | 0          | 0          | 1          |
| b6 (Pos 10) | 0          | 1          | 0          | 1          |
| b7 (Pos 11) | 1          | 1          | 0          | 1          |
R1 = b1, b2, b4, b5, b7
R2 = b1, b3, b4, b6, b7
R3 = b2, b3, b4
R4 = b5, b6, b7


![[Pasted image 20250411201506.png]]

R1 = 1, 0, 1, 0, 0 = 0
R2 = 1, 1, 1, 1, 0 = 0
R3 = 0 , 1, 1 = 0
R4 = 0, 1, 0 = 1

![[Pasted image 20250411201906.png]]

##### Vuelta
Rx
![[Pasted image 20250411202458.png]]

R1 = 1, 0,1 ,0, 1 = 1 (Mal)
R2 = 1, 1, 1, 1, 1 = 1 (Mal)
R3 = 0, 1, 1 = 0 (Bien)
R4 = 0, 1, 1 = 0 (Mal)

##### Errores en Rafagas
![[Pasted image 20250411203207.png]]
![[Pasted image 20250411203958.png | 450]]

Si ocurre un error en ráfaga de longitud k, cuando mucho se habrá afectado un bit de cada una de las k palabras codificadas.

Este método usa k*r bits de verificación para inmunizar bloques de k*m bits de datos contra un solo error en ráfaga de longitud k o menos.

##### Codigos de deteccion de Errores: Codigo de redundancia Ciclica  CRC
- m bits, coeficientes de polinomio de grado m-1, M(x) (el bit de mayor orden es el que se encuentra más a la izquierda)

- Polinomio generador G(x) de grado r

- Dividir  F(x)=x^rM(x)/G(x)

- T(x)=x^rM(x)-residuoF(x)

- Si T´(x)/G(x)=0, no hay errores E(x)

Código polinomial de r bits, detecta errores en ráfaga de longitud <=r

- M(X) Frame: 1101011011 

- G(X) Generador: 10011     

- X4M(X): 11010110110000

![[Pasted image 20250411205029.png]]

T(X) Frame transmitido:11010110111110

Frame original + suma de verificación

![[Pasted image 20250411205051.png]]

#### Ejemplo de bits en polinomios

**M(x)**
1001 -> $1X^3 + 0X^2 + 0X^1 + 0X^0$ -> $x^3 +1$
11011 -> $X^4 + X^3 + X + 1$
111111 -> $X^5 + X^4 + X^3 + X^2 + X + 1$

#### Ejemplo de como aplicar esta funcion
M(x)  = 1101011011 -> $X^9 + X^8 + X^6 + X^4+X^3+X+1$ -> $X^4 . M(x)$
M'(x) = $X^13+X^12+X^10+X^8+X^7+X^5+X^4$
M'(x) / G(x)
**G(x)** = 10011 -> $X^4 + X + 1$

# Foto del 11/04

## Protocolo Simplex para un canal con ruido

### ACK
#### Transmisor
- Transmite y espera (confirmacion o temporizador)
- Si expira el temporizador o confirmacion dañada, retransmite.
- Si confirma Ok aumenta el numero de secuencia y transmite la siguiente trama

#### Receptor
- Si llega la trama esperada, la pasa a la capa de red, aumenta el numero de secuencia y confirma la recepcion
- Si llega otra trama, la descarta y envia confirmacion de la ultima trama recibida correctamente

## Protocolo de ventana corrediza
- Bidireccionales intercalando datos y tramas de control (kind)
- Piggybacking o superposicion (ack)
	- es un ack bidireccional, osea emisor y receptor
- Numero de secuencia (0 a $2^n-1$)
#### Ventana emisora
N° de sec de la tramas enviadas pero no confirmadas

#### Ventana receptora
N° de sec de las tramas que puede aceptar o se espera recibir

ns = 0 - $2^n - 1$ -> 3 bits -> ns = 0 - 7

Protocolo de ventana corrediza de 1 bit
- parada y espera (numeros de sec 0 y 1)
- Duplex (Control y datos siempre disponibles)
- Ventana de tamaño uno
- ACK = ultimo n° de sec recibido bien
- Si los dos lados envian de manera simultanea una trama inicial, tenemos una situacion particular

![[Pasted image 20250423211050.png | 300]]

#### Retardo de propagacion
- Afecta a la eficiencia
- Utilizacion L/(L+bR)
- Canalizacion
- Manejo de errores

