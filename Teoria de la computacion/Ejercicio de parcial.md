
Sobre el alfabeto (a, b) cree una gramática tipo 3, por derecha, que genere palabras que comiencen con cero o más a o b, tengan 2 a en el centro y finalicen con cero o más a o b

Tipo 3
S -> aZ | aS | bS | bX
X -> aZ
Z ->  aC
C -> aC | bC | $\xi$

S -> bX -> baZ -> baaC -> baaC -> baaaC -> baaa$\xi$

S-> aZ -> aaC -> aa$\xi$

S -> bX -> baZ -> baaC -> baabC -> baab$\xi$

S -> bX -> 

baab

Tipo 2
S -> aZ | aS | bS | bX
X -> aaC  (X)
Z ->  aC
C -> aC | bC | $\xi$
