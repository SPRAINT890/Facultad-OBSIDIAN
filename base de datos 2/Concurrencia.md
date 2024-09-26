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

Estas funciones son secciones criticas y son unidades indivisibles, el DBMS genera una tabla de bloqueos y un subsistema gestor de bloqueos

#### Reglas para el bloqueo binario
Una transaccion T:
1. Debe ejecutar la operacion lock_item(X) antes de que se ejecute cualquier operacion read_item(X) o write_item(X) en T
2. Debe ejecutar la operacion unlock_item(X) despues de haber completado todas las operaciones read_item(X) y write_item(X) en T
3. No ejecutara una operacion lock_item(X) si ya posee el bloqueo del elemento X
4. No ejecutara una operacion unlock_item(X) a menos que posea el bloqueo del elemento X
##### Problemas
###### Demasiado restrictivos
Como máximo solo una transacción puede poseer un bloqueo sobre un elemento dado a la vez
###### Necesidades
Permite que varias transacciones tengan acceso al elemento X si todas ellas acceden a X solo para leer
Si una transacción va a escribir un elemento X, debe tener acceso exclusivo a X


## Bloqueo Multiples Lectura/Escritura
Tiene 3 estados
- read-locked/share-locked
- write-locked/exclusive-locked
- unlocked

### Implementacion
Mantener el numero de transacciones que poseen un bloqueo compartido
Tabla de bloqueos con 4 campos:
- data_item_name

```shell
B: if lock(X) == "unlocked" then
	begin
		lock(X) = "read-locked";
		no_of_reads(X) = 1;
	end
else
	if lock(X) == "read-locked" then
		no_of_reads(X) = no_of_reads(X) + 1;
	else
		begin
			wait (until LOCK)
```

##### write_lock(X)
```shell
B: if lock(X) == "unlocked" then
	lock(X) = "write-locked";
else
	begin
		wait (until lock(X))
```

#### Reglas para el bloqueo lectura/escritura
Una transaccion T:
1. debe ejecutarse la operacion read_lock(X) o write_lock(X) antes de que se ejecute cualquier operacion read_item(X) en T
2. debe ejecutar la operacion write_lock(X) antes de que se ejecute cualquier operacion write_item (X) en T
3. debe ejecutar la operacion unlock(X) despues de haber completado todas las operaciones read_item(X) y write_item(X) en T
4. no ejecutara una operacion read_lock(X) si ya posee un bloqueo de lectura  o de escritura para el elemento x
5. no ejecutara una operacion write_lock(X) si ya posee un bloqueo de lectura o de escritura para el elemento x
6. no ejecutara una operacion unlock(X) a menos que posea un bloqueo de lectura o de escritura sobre el elemento X

#### Conversión de bloqueos
- A veces se quieren hacer menos estrictas las reglas 4 y 5
- para ello se permite la conversion del bloqueo
	- una transaccion T ejecuta la operacion read_lock(X) y mas adelante solicita promocionar el bloqueo ejecutando una operacion write_lock(X)
	- si T es la unica transaccion que posee un bloqueo de lectura sobre X, entonces el bloqueo puede promocionarse
	- en caso contrario la transaccion T debe esperar
- Cuando se permite la conversion de bloqueos, la tabla de bloqueo debe incluir un campo transacciones_bloqueos para guardar los identificadores de transacciones

