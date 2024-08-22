## Ejercicio Profe 1
$R_1$  (A, B, C, D, E, G, H)

$F_1$  {AB -> CDE, C -> A, D -> E, H -> E, HE -> G}

#### Hallar **todas** las claves de R1

##### Observación:
Los atributos B y H solo aparecen del lado izquierdo de la DF (Dependencia Funcional), por ende solo se puede llegar a ellos si son parte de la clave de $R_1$

Si $(BH)^+$ = $R_1$,  entonces BH es clave

$BH^+$ {B, H, E, G} $\neq R_1$ -> BH  no es clave

Como G solo aparece del lado derecho de las DF, sabemos que no va a formar parte de ninguna clave mínima

##### ¿Cuales son las combinaciones posibles con 3 atributos de $R_1$?
1. $(BHA)^+$ = {B, H, A, C, D, E, G} $\surd$
2. $(BHC)^+$ = {B, H, C, A, D, E, G} $\surd$
3. $(BHD)^+$ = {B, H, D, E, G} X
4. $(BHE)^+$ = {B, H, E, G} X

##### ¿De cuatro?
$(BHDE)^+$ = (B, H, D, E, G) -> No es clave

## Ejercicio Profe 2
$R_2$ (A, B, C, D, E, G)
$F_2$ {B -> CD, ACD -> B, C -> AE}

#### Hallar **todas** las claves de R2 justifique!
$A^+$ = {A}
$B^+$ = {B, C, D, A, E}
$C^+$ = {C, A, E}
$D^+$ = {D}
$E^+$ = {E}
$G^+$ = {G}
$(BG)^+$ = {B, C, D, A, E, G} $\surd$
$(ACG)^+$ = {A, C, E, G}
$(CGD)^+$ = {C, G, D, A, E, B} $\surd$
$(ACDG)^+$ = {A, C, D, G, B, E} $\surd$

BG, CGD y ACDG son las claves ya que no quedan atributos que no se repitan para formar una clave



## Ejercicio 1

![[Pasted image 20240822181859.png]]

A -> B
A -> C
C -> D
C -> G
BD -> E
AB -> D
BC -> G
#### A
$A^+$ {A, B, C, D, G, E}
$BG^+$ {B, G}
No cumple por que la cobertura de BG no llega a D
#### B
$C^+$ = {C, D, G}

Es verdadero ya que todas las clausulas de los atributos de la derecha llegan a los de la izquierda

## Ejercicio 2
Dado el esquema de relacion
	R = (A, B, C, D, E, G)
Y el conjunto de DF
	F = {AE -> BD, AB -> CEG, EG -> BC, B -> A, G -> D}
Determinar la forma normal de la siguiente descomposición
	D = {R1(A, B, C, D) 
		R2(B, C, D, E, G)}

### Forma normal de R1

##### F1
AB -> C
B -> A
D -> D

###### ¿Cuál es la clave de R1?
$BD^+$ = {A, B, C, D}

###### DF1
AB -> C
B -> A
![[tempFileForShare_20240822-202609.jpg]]