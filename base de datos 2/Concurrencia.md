Se necesita garantizar la ausencia de interferencia y la propiedad de aislamiento.

Existen 4 tipos de técnicas para ordenar las transacciones

- Bloqueo
- Marcas de tiempo
- Multiversión
- Validación o certificación

## Granularidad
Que voy a tomar yo como elemento para aplicar estas tecnicas.
EJ
tablas, bd, celda de una tabla, etc

## Bloqueo en dos fases
Un bloqueo es una variable asociada a un elemento de datos que describe el estado de ese elemento respecto a posibles operaciones que se le pueden aplicar

### Técnicas
- Binario
- Lectura/Escritura (Share/Exclusive)
	- Modo lectura: Solo se puede leer el registro y es compartido
	- Modo Escritura: nadie puede hacer nada
	- No esta bloqueado

## Bloqueo Binario
Tiene dos estados
- Lock (1)
- Unlock (0)
Cada elemento X de la base tiene un bloqueo distinto
Lock (X) Valor actual del bloqueo del elemento X

##### Función
```bash
lock_item (X)
	B: if lock (X) = 0 then
		lock (X) = 1
	else
		wait (lock (X) = 0)
		goto B

unlock_item (X)
	lock (X) = 0
	signal (lock(X) = 0)
```
