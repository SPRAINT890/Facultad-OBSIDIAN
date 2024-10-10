
## Primario o Principal
- Memoria RAM
- Memoria Cache

## Secundario
- Disco duros o SSD

## Terciario
- Unidades extraíbles
- Cintas Magnéticas


## Diseño Fisico
- Tablespace - Contenedor
	Se le puede asignar varios contenedores para esparcir los datos en varios discos, haciendo que sea mas rapido la lectura de la informacion de una tabla.

- Indices
	Son indices con estructuras paralelas a la original, la cual facilita la busqueda de un valor sobre el mismo elemento del indice.
	- Tener muchos indices genera ineficiencia de espacio y consume tiempo de actualizacion de los indices

-  Politica de respaldo

## Manejo de Buffer

### Estrategia de remplazo
#### Dirty Bit
Hay un bit reservado llamado dirty bit, que indica si tiene información actualizada, entonces tiene que guardar la informacion de ese bloque antes de borrarla.

- LRU (Less Recently Used)
	Es el bloque el cual fue usado hace mas tiempo
- Clock Policy
	Ordena los bloques segun el uso en un circulo
- FIFO
	First In First Out

### Salida Forzada de bloques
- Recuperacion de transacciones
	Se le pone un Time Stamp donde cada tanto se guarda los bloque de la memoria en disco, para tener una recuperacion de estos bloques en caso de alguna falla

### Bloques Sujetos

## Organización de Archivos


- Registros de Longitud Fija