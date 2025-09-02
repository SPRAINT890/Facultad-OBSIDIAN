
## 1 Con los conocimientos actuales sobre Teoría de Conjuntos, máquinas de estado y autómatas finitos, comente con sus palabras qué utilización le encuentra a definición de conjunto, pertenencia de elementos y a las operaciones de unión, intersección y complemento? Si lo considera necesario, amplíe con otros conceptos vistos en el repaso de Teoría de Conjuntos.

## 2 Indique si es verdad {1, {2,3}} = {{3,2},1}
Es verdad ya que en teoria de conjuntos los conjuntos no estan ordenados, por ende la distribucion de los elementos del conjunto no perjudica


## 3 ¿Qué se obtiene con las siguientes operaciones sobre conjuntos? 
{1, 2, 3} $\cup$ {3, 4} = {1, 2, 3, 4}
![[Pasted image 20250821193856.png]]
{1, 2, 3} $\cap$ {3, 4} = {3}
![[Pasted image 20250821194019.png]]

{1, 2, 3} - {3, 4} = {1, 2}
![[Pasted image 20250821194124.png]]

{1, 2, 3} - {4, 5} = {1, 2, 3}
![[Pasted image 20250821194155.png]]

{1, 2} X {3, 4, 5} = {(1, 3), (1, 4), (1, 5), (2, 3), (2, 4), (2, 5)}


Grafíquelo con diagramas de Venn

## 4 Cómo se lee {$0^n$ $1^n$ | n ≥ 1} y de qué cadenas consta su lenguaje

Toda las cadenas de la forma $0^n 1^n$ tal que $n \geq 1$  y consta de cadenas de 0 y 1; y que no pueden ser intercambiados entre si, siendo que sean la misma cantidad de 0 que de 1
Ejemplo
01, 0011, 000111, .....

## 5 De qué cadenas consta el lenguaje {$0^i$ $1^j$ | 0 ≤i≤ j}
La cadena es tal que asi:
	01, 011, 0111, 00111

Haciendo que 0 tenga que aparecer igual veces o menos que 1 con un limite de 0

## 6 En {x 01y | x e y son cadenas cual quiera formadas por 0s y 1s} De ejemplos de cadenas pertenecientes al lenguaje anterior y de otras no pertenecientes
Pertenecientes: 
000001111111, 100010

No Pertenecientes
7777018888, 1111111111, 1100

## 7 Qué significa el lenguaje L = {w $\in$ {0, 1}$^*$ | ceros (w) = unos (w)}
Son cadenas de 0 y 1 sin importar el orden de los valores solo que haya la misma cantidad de ceros que de unos, dando una suma de valores pares, incluyendo el conjunto vacio
	Ejemplo
		01, 10, 1010, 0101, 011100,

## 8 Si L = {ab,c} es lenguaje sobre el alfabeto {a,b,c} De ejemplos de $L^0$ , $L^1$ , $L^2$ , $L^3$

$L^0$ = {$\epsilon$}
$L^1$ = {ab, c}
$L^2$ = {ab, c} {ab, c} = {abab, abc, cab, cc}
$L^3$ = {ab, c} {ab, c} $L^1$ = {abab, abc, cab, cc} {ab, c} = {ababab, ababc, abcab, abcc, cabab, cabc, ccab, ccc}

## 9 Qué significa L = {$W$ $\in$ {a,b}$^*$ | $W =$ $W^R$ } Qué gramática genera este lenguaje?

Significa que el leguaje L contiene a, b y conjunto vacio tal que las combinaciones de de estas letras generen palabras palindromes

$G_l$ = (V, T, P, S)
V = {S}
T = {a, b}
P = S -> aSa | bSb | a | b | $\epsilon$

## 10 Lo que sigue son reglas de producción de un lenguaje. ¿Cómo se lee? 
`{programa} ::= [<cabecera>] begin <sentencia> end <sentencias> ::= <sentencia> {<sentencia>}`
En un programa, con un nombre y puede tener una cabecera que es opcional, seguido de un begin con una o mas sentencias y finaliza con un end

## 11

## 12 ¿Cuál es el conjunto de símbolos para derivar frases en castellano?
`P = {[A-Z], [a-z], ' ', [?, !]}`

## 13 Defina un lenguaje que considere las matrículas de auto en Uruguay
`L = { W | W [A, B, C, D, ... S], [A-Z] [A-Z] [0-9] [0-9] [0-9] [0-9]}`

## 14 Obtener los 5 elementos más breves de {b,aa}$^+$. Qué pasaría si fuese * en lugar de +?
b, bb, aa, bba, aab.
si fuera * en vez de + tendria que agregar el conjunto vacio.

## 15 El lenguaje de todas las cadenas que constan de n ceros seguidos de n unos para cualquier n ≥ 0

L = {W | W $\in$  $0^n 1^n$ $n \geq 0$}

$\epsilon$, 01, 0011

S -> 0S1 | $\epsilon$

## 16 El conjunto de cadenas formadas por el mismo número de ceros que de unos

L = {W | W $\in$ {0,1}* ceros (w) = unos (w)}

## 17 De una gramática que genere números entre 0 y 128
G = {}
V = {S, A, B}
T = {1, 2, 3, 4, 5, 6, 7, 8, 9, 0}
P
S

S -> 0 | 10X | 11X | 12Z
X -> 0-9
Z -> 0-8

## 18 Obtener derivaciones de 002 y 0001 a partir de la GR ({0,1,2}, {A,B}, A, {A -> 2 | 0B, B ->1 | 0A}) ¿Qué lenguaje genera?

GR = ({A, B}, {0, 1, 2}, {P, A})
A -> 2 | 0B 
B ->1 | 0A

![[Pasted image 20250902190838.png]]
L = { $0^n 2$ | n par $\geq$ 0} $\cup$ {$0^m1$ | m > 0}

## 19
ac, abc, abbc, ...

G = (V, T, P, S)

tipo 3
S -> aH
H -> bH
H -> c

otra

tipo 2
S -> ac | aXc
X -> b | bX

## 20 Dada la gramática ({a,b}, {I,X,V,Y}, I, P) con P dada por $I ->$ VXY | XV, X -> VI|YIV | $\lambda$ , VY -> YV, YV -> VY, V -> a, Y -> b | $\lambda$ Indique tipo, derive ababa e indique que lenguaje genera

I -> VXY | XV
X -> VI | YIV | $\lambda$ 
VY -> YV
YV -> VY
V -> a
Y -> b | $\lambda$

I -> V 

Son palabras que contienen