Objetivos:
- Forense Digital: preservar la evidencia en su forma original, analizarla y presentar los hallazgos
- respuesta a incidentes: gestionar la situación

herramientas y técnica:
- FD: diseñadas para la recuperación de datos, el análisis de discos y memorias, la extracción de datos y su análisis
- RI: aprovecha los sistemas de deteccion de intrusiones (IDS), threat intelligence y otras herramientas de monitoreo en tiempo real

Resultado
- FD: produce evidencia que se puede utilizar en procedimientos legales o para obtener u conocimiento profundo de un incidente de seguridad
- RI: da como resultado la resolución inmediata ante una amenaza, con estrategias para prevenir sucesos futuros



- Identificación: es el proceso que implica detectar y verificar incidentes. se debe determinar el alcance del incidente e incluir a las personas y procesos asociados
- alcance: implica definir que elementos de la infraestructura están comprometidos, junto a sus dependientes
- impacto: puede medirse teniendo en cuenta diferentes criterios como:
	- la magnitud de los daños
	- la duración de la interrupcion
	- el coste de recuperacion
	- las implicaciones legales o reputacion

## Monitoreo y Observabilidad
- Monitoreo: el monitoreo es el proceso de recolección, análisis y uso de informacion para hacer un seguimiento del progreso de un determinado sistema
- Observabilidad: es la capacidad de comprender el estado interno de un sistema mediante el análisis de los datos que genera, como logs, métricas y trazas (Teoria de control)
### Monitoreo y Seguridad
- es un proceso automatizado de recopilación de datos de seguridad que indican posibles amenazas. este proceso genera y prioriza alertas para que una organización pueda responder según sea necesario
- Tipos de monitoreo:
	- Telemetría: se utiliza para recopilar, registrar y analizar datos de los sistemas para comprender como funcionan
	- Monitoreo de logs e inteligencia de amenazas: Implica la identificación y análisis de indicadores de compromiso (IoC), que son los signos o pruebas de que se ha producido o se esta produciendo un ataque

- Tipos de monitoreos (por objetivos)
	- Monitoreo de endpoints: son dispositivos conectados a una red.
	- Monitoreo de red: se rastrean y analizan actividades sobre la red para encontrar y responder a problemas
	- Monitoreo de aplicaciones:}

### Observabilidad y seguridad
- No es un objetivo en si, sino una practica para alcanzar determinados requerimientos
- Componentes claves
	- Metricas
	- Logs
	- Trazas: busca determinar un flujo a medida que se pasa de una parte del sistema a otra. Proporcionan direccionalidad y relaciones entre dos puntos, se logra agregando una identificación de seguimiento medida que la solicitud/acción fluye en el sistema
	- Eventos: Los eventos registran acciones especificas, se utiliza para aumentar la capacidad de Observabilidad. por ejemplo, cada vez que un usuario administrador ejecuta una tarea privilegiada, el sistema registre un evento. analizados a lo largo del tiempo, los eventos pueden ayudar a determinar patrones

### Herramientas de observabilidad y monitoreo
- SIEM
	- Recopila y analiza infornacion de diferentes fuentes
- EDR
	- proporciona la capacidad de supervisar los endpoints en busca de comportamientos sospechosos
- SOAR
	- combina automatizacion y la orquesta

### Tipos de Dispositivos
- Switches: el trafico que se origina en un host y sale de la red interna atravesara varios switches. los switches manejan tablas que pueden ayudar a rastrear conexiones (pe: ARP)
- Router: permiten las conexiones entre LANs y/o WAN. Manejan trafico, insumo importante la tabla de ruteo
- Firewall: se encargan del filtrado de paquetes y son una amplia fuente de informacion mediante la geracion de logs
- Web proxy/proxy reverso: estos dispositivos pueden brindar una vision del trafico web de toda la organizacion. Tanto el que se origina en la organizacion como el; dirigido a hosts internos
- DHCP

## Evidencia de red: recaudos
- Crear y mantener actualizado un diagrama de red, es una buena ayuda al momento de gestionar incidentes
	- el diagrama debe ser lo suficientemente detallado como para que IRT pueda identificar componentes de red individuales (switches, router, APs, firewall)
	- deberia contener direcciones IPs internas para que el IRT pueda acceder a esos sistemas
- Configuraciones de dispositivos:
	- Las organizaciones deberian contar con respaldos de las configuraciones de dispositivos de red
	- esto proporciona una linea base ante modificaciones y un mecanismos de recuperacion

## Adquisicion de evidencia HOST
- Vision general:
	- Los sistemas puestos de trabajo o servidores representan un posible objetivo inicial para que alguien pueda ganar acceso (pivote)
	- El IRT debe estar preparado para adquirir diferentes tipos de evidencia de este tipo de sistemas
	- es importante adquirir de acuerdo al orden de volatilidad
	- es fundamental que las herramientas que se seleccionen para la adquisicion de evidencia sean proporcionadas por fuentes confiables
	- los encargados de responder a incidentes deben contar con las credenciales de acceso necesarias para realizar estas tareas

Volatility