
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
	si hay cache mios
		calculo
	y guardo en el cache
	retorno bucle

##### Con cero en el cache
funcion_aux(i, c)
	observo el cache
	if i = 0
		valor = 0

#### Bottom Up
bottom_up_pd(count, c)
	1) pd: [ ] x 21 (o tamaño de los problemas)
	2) caso base
	3) For de bottom_up -> resuelve todos los problemas mas chicos (puede ser mas de uno
		a = -inf
		for c in coins:
			var as min (a, pd (i-c))
			pd[i] = valor calculado
	 4) return pd

# 