## Normalización
nivel y metodología de diseño
- metodología ascendente (bottom up), a partir de los atributos buscando la relacion de todo con todo y verificar que pertenecen a la misma entidad.
- metodología descendente, partimos de ciertos agrupamientos
[[Normalización]]
## dependencia funcional
R es una tabla universal con todos los atributos de la realidad

X -> Y

### Ejemplo
CI -> Nombre
CI -> CodSocio
CI -> Telefono
CI -> Tipo Sangre
~~Nombre -> CI~~

CI -> {Nombre, CodSocio, Telefono, Tipo Sangre}

Direccion -> cod_postal

### Reglas de inferencia
1. Reflexiva: $si, X \supseteq Y entonces X -> Y$
 
2. Aumento: ${x \rightarrow} = xz \rightarrow yz$
   Titulo -> Genero
   {Titulo, Autor} -> {Genero, Autor}
3. Transitiva: ${x \rightarrow y, y \rightarrow z} = x \rightarrow z$
   Titulo -> Autor
   Autor -> IdiomaOrigen
   Titulo -> IdiomaOrigen

4. Descomposición: ${x \rightarrow yz} = x \rightarrow y$
5. Unión o aditiva ${x \rightarrow y, x \rightarrow z} = x \rightarrow yz$
   Titulo -> Autor, Titulo -> Editorial = Titulo -> {autor, editorial}
6. Seudotransitiva ${x \rightarrow y, wy \rightarrow z} = wx \rightarrow z$
   ISBN -> Titulo
   {Autor, Titulo} -> Genero
   {Autor, ISBN} -> Genero

## Clausura del conjunto de dependencias funcionales

F = {DNI -> Nombre,
	NumProyecto -> {NombreProyecto, UbicacionProyecto}
	{DNI, NumProyecto} -> Horas}

$F^+ = F + DF$ (Dependencias Funcionales) , Producto de aplicar las reglas de Inferencia
ej
	A $\rightarrow$ E, B, C
	BC $\rightarrow$ L, G, E
	$A^+$ (A, B, C, E, L, G) $\rightarrow$ Esto es la cobertura mínima

### Clausura de $X, X^+$

#### Algoritmo para calcular $X^+$ :
	$X^+ := X$
	Repetir
		antigua $X^+ := X^+$
		para cada DF $X \rightarrow Z$ en F ejecutar
			si $X \supseteq Y$ entonces $X^+:X \cup Z$
	Hasta que $(X^+ = antigua$ $X^+)$		

$DNI^+ = {DNI, nombre}$
$NumProyecto^+ = {NumProyecto, UbicacionProyecto}$
${DNI, NumProyecto}^+ = {DNI, NumProyecto, Horas, Nombre, NombreProyecto, UbicacionProyecto}$

### Cobertura
Def: Se dice que un conjunto de dependencias funcionales F cubre a otro conjunto de dependencias funcionales E, si toda dependencia funcional de E está también en $F^+$

Def 2: Se dice que dos conjuntos de dependencias funcionales E y F son equivalentes si $E^+ = F^+$ O sea, dada una DF de E puede inferirse de F y viceversa

### Cobertura mínima
Def: Una cobertura mínima de un conjunto de dependencias funcionales E, es un conjunto dependencias funcionales F que satisface la propiedad de que cada dependencia de E está en la clausura $F^+$ de $F$

Def 2: Además, está propiedad se pierde si se elimina cualquier dependencia del conjunto F

Ejemplo
$F^+$ = {DNI -> Nombre,
	NumProyecto -> {NombreProyecto, UbicacionProyecto},
	{DNI, NumProyecto} -> Horas,
	{DNI, NumProtecto} -> {DNI, Nombre, NombreProyecto, UbicacionProyecto, Horas, NumeroProyecto}} 

[[Anotación Canónica|Anotación Canónica]]	

E = {{DNI, NumProyecto} -> * }

[[Ejemplo de Cobertura Minima]]


