
## 1
Con los conocimientos actuales sobre Teoría de Conjuntos, máquinas de estado y autómatas finitos, comente con sus palabras qué utilización le encuentra a definición de conjunto, pertenencia de elementos y a las operaciones de unión, intersección y complemento? Si lo considera necesario, amplíe con otros conceptos vistos en el repaso de Teoría de Conjuntos.

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

## 7 Qué significa el lenguaje L = {w $\in$ {} | ceros (w) = unos (w)}