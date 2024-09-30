1. Dadas las siguientes afirmaciones respecto a requisitos, seleccione la opcion correcta
	D. El costo de corrección de error en los requisitos es mas alto si este se detecta luego de la puesta en producción que en etapas tempranas como el relevamiento.
2. C
3. A
4. B
5. D
6. B
## Practico
![[Pasted image 20240927191455.png | 500]]

Caso de Uso Reservar
Nombre: Generar reserva

Descripción: Le permite a un usuario generar una reserva

Pre-condición:
- Navegador con internet
- Existe un concierto
- Usuario Logeado

Post-condición:
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



Requisitos No Funcionales
- Seguridad en los metodos de pagos
- Seguridad en los datos personales de los usuarios
- Tiene que soportar grandes volumenes de carga de usuarios
- Interoperabilidad con sistemas de pago como visa, mastercard o paypal
- Gran compatibilidad con la mayoria de telefonos
- Web responsibe

Requisitos funcionales
- ABM De usuarios
- ABM De concierto
- Sistema de pago
- Sistema de reserva

Historia de usuario
Rol: Cliente
- Como cliente, quiero poder pagar con tarjeta de debito la reserva de los conciertos
- Como cliente, quiero poder autentificarme con mi cuenta de Google para mayor rapidez
- Como cliente, quiero poder cancelar una reserva en caso de arrepentimiento