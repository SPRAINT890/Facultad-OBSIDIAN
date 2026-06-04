Algoritmo de Grafos:

G = {V, E}
	(Vertices y Aristas)

foto (04 06)
Matriz para poco disperso


### Algoritmo de busqueda

Navego por las aristas para encontrar otros vertices

#### BFS -> Breadth First Search
Tiene una frontera de descubrimiento
Colores de los vertices: Blanco (No fue descubierto), Gris (Fue descubierto), Negro (Todos sus hijos fueron descubiertos y por ende no estan en la frontera)
Cuando empieza empiezan todos blancos, pero cuando termina no necesariamente quedan todos negros, por que puede haber un nodo sin camino

Queue FIFO
#### DFS -> Depth First Search