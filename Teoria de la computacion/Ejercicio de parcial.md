
Sobre el alfabeto (a, b) cree una gramática tipo 3, por derecha, que genere palabras que comiencen con cero o más a o b, tengan 2 a en el centro y finalicen con cero o más a o b

S -> X | aS | bS | v
X -> aZ
Z ->  aC
C -> aC | bC | 0 | $\epsilon$

