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
![[tempFileForShare_20240822-202609.jpg]]


### Forma normal de R2
##### F2
EG -> B
EG -> C
G -> D

###### ¿Cuál es la clave de R2?
$EG^+$ = {E, G, B, C, D}

###### DF2
![[tempFileForShare_20240822-204413.jpg]]

## Ejercicio 4
#### A
F {A $\rightarrow$ BC, CD $\rightarrow$ E, B $\rightarrow$ D, E $\rightarrow$ A}

$A^+$ (A, B, C, D, E) $\checkmark$
$E^+$ (E, A, B, C, D) $\checkmark$
$B^+$ (B, D) X
##### Los de 2 no pueden tener ni A ni E
$CD^+$ (C, D, E, A, B) $\checkmark$
$BC^+$ (B, C, D, E, A) $\checkmark$


#### B
$R_1$ (A, B, C)
$R_2$ (A, D, E)

($R_1 \cap R_2)$ $\rightarrow$ ($R_1 - R_2$) $= A \rightarrow B C$
($R_1 \cap R_2$ ) $\rightarrow$ ($R_2 - R_1$)

#### C
$R_1$ (A, B, C)
$R_2$ (C, D, E)

($R_1 \cap R_2)$ $\rightarrow$ ($R_1 - R_2$) $= C \rightarrow A B$
($R_1 \cap R_2$ ) $\rightarrow$ ($R_2 - R_1$) $= C \rightarrow D E$

##### No cumple por que estas dependencias funcionales no son parte de la F

###### Ejemplo de cobertura de F
![[Pasted image 20240829201956.png | 500]]


## Ejercicio de Parcial
- G y H debe formar parte de la clave, pues no están en ninguna DF

A) Tenemos esquema y F, siempre es posible determinar las claves -> Falso

B) $AB^+ \rightarrow$ (A, B, C, D) $\neq R \rightarrow$ Falso

C) $IGH^+ \rightarrow$ (I, A, E, J, K, L, B, C, D, G, H), Cualquier clave debe tener I, porque $I \rightarrow AEJKL$ es la única DF que determina J.

D) $BGH^+ \rightarrow$ (B, G, H) $\rightarrow$ Falso

## Ejercicio 5
### A)
DNI - A
NombEmpl - B
NumProy - C
UbicProy - E
Horas - G
NombProy - D


R (A, B, C, D, E, G)
F = {$A \rightarrow B, C \rightarrow DE, AC \rightarrow G$}

a) A y C en todas las claves, porque solo aparece del lado izq de las DF
G no aparece en ninguna clave, porque solo aparece del lado derecho de las DF

$AC^+$ (A, C, B, D, E, G)

Las claves de 3 deben contener A, C . So los contienen son superclaves, pues AC es clave

### B)
$R_1$ (A, B), $R_2$ (C, D, E), $R_3$ (A, C, G)

R = $R_1 * R_2 * R_3$, propiedad de JSP

#### Verificar Concatenacion sin perdida MULTIPLE

|     | A        | B        | C        | D        | E        | G        |
| --- | -------- | -------- | -------- | -------- | -------- | -------- |
| R1  | $B_{11}$ | $B_{12}$ | $B_{13}$ | $B_{14}$ | $B_{15}$ | $B_{16}$ |
| R2  | $B_{21}$ | $B_{22}$ | $B_{23}$ | $B_{24}$ | $B_{25}$ | $B_{26}$ |
| R3  | $B_{31}$ | $B_{32}$ | $B_{33}$ | $B_{34}$ | $B_{35}$ | $B_{36}$ |

|     | A        | B        | C        | D        | E        | G        |
| --- | -------- | -------- | -------- | -------- | -------- | -------- |
| R1  | A1       | A2       | $B_{13}$ | $B_{14}$ | $B_{15}$ | $B_{16}$ |
| R2  | $B_{21}$ | $B_{22}$ | A3       | A4       | A5       | $B_{26}$ |
| R3  | A1       | $B_{32}$ | A4       | $B_{34}$ | $B_{35}$ | A6       |

|     | A        | B        | C        | D        | E        | G        |
| --- | -------- | -------- | -------- | -------- | -------- | -------- |
| R1  | A1       | A2       | $B_{13}$ | $B_{14}$ | $B_{15}$ | $B_{16}$ |
| R2  | $B_{21}$ | $B_{22}$ | A3       | A4       | A5       | $B_{26}$ |
| R3  | A1       | A2       | A4       | $B_{34}$ | $B_{35}$ | A6       |

|     | A        | B        | C        | D        | E        | G        |
| --- | -------- | -------- | -------- | -------- | -------- | -------- |
| R1  | A1       | A2       | $B_{13}$ | $B_{14}$ | $B_{15}$ | $B_{16}$ |
| R2  | $B_{21}$ | $B_{22}$ | A3       | A4       | A5       | $B_{26}$ |
| R3  | A1       | A2       | A3       | A4       | A5       | A6       |

![[Pasted image 20240829201844.png | 500]]