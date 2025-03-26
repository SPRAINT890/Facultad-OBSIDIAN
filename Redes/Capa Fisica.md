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