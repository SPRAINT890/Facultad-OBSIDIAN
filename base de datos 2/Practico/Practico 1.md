## Ejercicio Profe
$R_1$  (A, B, C, D, E, G, H)

$F_1$  {AB -> CDE, C -> A, D -> E, H -> E, HE -> G}

#### Hallar **todas** las claves de R1

##### Observación:
Los atributos B y H solo aparecen del lado izquierdo de la DF (Dependencia Funcional), por ende solo se puede llegar a ellos si son parte de la clave de $R_1$

Si $(BH)^+$ = $R_1$,  entonces BH es clave

$BH^+$ {B, H, E, G} $\neq R_1$ -> BH  no es clave

Como G solo aparece del lado derecho de las DF, sabemos que no va a formar parte de ninguna clave mínima

##### ¿Cuales son las c?
1. (BHA)
2. (BHC)
3. (BHD)
4. (BHE)


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