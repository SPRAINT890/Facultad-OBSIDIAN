1. Dadas las siguientes afirmaciones respecto a requisitos, seleccione la opcion correcta
	D. El costo de correccion de error en los requisitos es mas alto si este se detecta luego de la puesta en produccion que en etapas tempranas como el relevamiento.
2. C
3. A
4. B
5. D
6. B
## Practico
![[Pasted image 20240927191455.png | 500]]

Caso de Uso Reservar
Nombre: Generar reserva

Descripcion: Le permite a un usuario generar una reserva

Pre-condicion:
- Navegador con internet
- Existe un concierto
- Usuario Logeado

Post-condicion:
- El usuario es redirigido a pagina principal con una reserva por confirmar

Flujo Normal:
1. El usuario busca conciertos
2. El sistema, muestra un listado de conciertos disponibles
3. El usuario, selecciona un concierto de la lista para reservar
4. Sistema, muestra los datos y ubicaciones del concierto, solicita cantidad de entradas
5. usuario Selecciona ubicaciones y cantidad de entradas y confirma.
6. Sistema guarda la reserva y redirige a la pagina principal
7. Fin CU

Flujo Alternativo
	No existe concierto
		3.1: El usuario vuelve al inicio
		3.2: Fin CU
	Ubicaciones no disponibles
		6.1: El sistema muestra que la ubicaciones seleccionada no esta disponibles
		6.2: vuelvo a 4 FN
