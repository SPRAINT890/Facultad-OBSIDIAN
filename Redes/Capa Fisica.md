## Objetivo
- **Transmitir** de bits "Puros" a traves de un canal de comunicacion, como cable utp, fibra, wifi, etc
- Los aspectos del diseño tienen que ver con interfaces mecanicas, electricas, de temporizacion y ademas con el medio fisico de transmision que esta bajo la capa fisica.
	- Cuantos pines tiene el cable
	- La forma del cable
	- Estandarizar los conectores
	- Como se representa un 1, ya sea por un pull up (mandar 5v) o por un pull down (0v o -5v)
	- Lidiar con las limitantes de los medios fisicos, tales como el ancho de banda, ruido de la red, etc.

### Analisis de la transmision de datos
- Mediante el cambio de simbolos ya sea por picos o por diferencia de frecuencia de los picos
- Se pueden usar varios simbolos, para representar 2 pares de bits, ya sea por diferente voltaje o por picos con diferente frecuencia
- Para saber cuantos simbolos necesito esta este calculo $2^M$ siendo M la cantidad de bits que quiero representar
- Los medios tienen un limite de ancho de banda, que depende de la rapidez de la variacion de bits, el cual puede generar valores de bits falsos
#### Ancho de banda
- el ancho de banda depende de la longitud del medio
- unidad de ancho de banda heartz por segundos
- tasa de datos bits, megas, etc

## [[Teorema de Nyquist |Teorema de Nyquist]]
Dado un canal sin ruido de ancho de banda B, el receptor puede reconstruir por completo la señal transmitida tomando solo 2B muestras por segundo.

De esta forma el ancho de banda disponible B es una limitante dado que la cantidad de simbolos por segundos (**Baudios**) r debe cumplir la siguiente relacion.

$R \leq 2B$

Si tenemos una cantidad de M simbolos cada uno de estos puede representar a N bits donde $N = log2M$ (Bits por simbolo)

Tasa de datos maxima = $2B$ $log_2M$ bits/seg

## [[Teorema de Shannon |Teorema de Shannon ]]
Otra limitante es el ruido presente en el canal, el mismo es medido por la relacion entre la potencia de la señal y la potencia del ruido S/N.
En general, se da la cantidad de decibeles (10 $log_{10}$ S/N)

En este caso la tasa de datos maxima queda expresada de la siguiente forma

Numero maximo de Bits/Seg = B $log_2$ (1 + S/N)

## [[Medios de Transmision |Medios de Transmision]]