
PD -> CACHE <- top down
    -> ARRAY (matriz en bottom up)

## Coin change
F 0 si i=0
#### Top down
Observo si el valor esta en el cache y si no computo
'Descubro problemas mas chicos'

Funcion(parametros del problema)
	Funcion_aux(Parametro del problema, cache)
La primera funcion se encarga de inicializar el cache, mientras que la funcion chica le pasamos los parametros y el cache

##### Sin cero en la cache
funcion_aux(i, c)
	if i = 0
		return 0
	observo cache
	si hay cache mis
		calculo
	y guardo en el cache
	retorno bucle

##### Con cero en el cache
funcion_aux(i, c)
	if i = 0
		valor = 0

#### Bottom Up
funcion_bottom_up
	dp = inicializar