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

```python
def bfs(grafo, inicio):
    color = {}
    distancia = {}
    padre = {}
	
	#Seteo de nodos como no descubiertos
    for nodo in grafo:
        color[nodo] = "BLANCO"
        distancia[nodo] = float("inf")
        padre[nodo] = None
	
	#asigno el primer nodo como gris distancia 0
    color[inicio] = "GRIS"
    distancia[inicio] = 0

    cola = deque()
    cola.append(inicio)

    while cola:
        u = cola.popleft()

        for v in grafo[u]:
            if color[v] == "BLANCO":
                color[v] = "GRIS"
                distancia[v] = distancia[u] + 1
                padre[v] = u
                cola.append(v)

        color[u] = "NEGRO"

    return distancia, padre, color
```
#### DFS -> Depth First Search