
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
