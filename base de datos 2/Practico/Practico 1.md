## Ejercicio Profe
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
$(BHDE)^+$ = 


## Ejercicio 1

![[Pasted image 20240822181859.png]]

A -> B
A -> C
C -> D
C -> G
BD -> E
AB -> D
BC -> G

$A^+$ {A, B, C, D, G, E}
$B^+$ {

}