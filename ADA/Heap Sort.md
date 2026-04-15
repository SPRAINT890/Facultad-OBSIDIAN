
1) Orden de O$(n \log n)$
2) in place
3) Utiliza una estructura de datos: heap (Max-heap o Min-Heap)

![[Pasted image 20260414203408.png]]

array length es el tamaño del array del heap
Array Heap Size es hasta donde va el heap 

la mitad del heap son hojas la otra son nodos

```python
A[Parent(i)] >= A(i) -> Max_heap para todo i
A[Parent(i)] <= A(i) -> Min_heap para todo i
```

```python
Max_heapify(A, i)
	l = left(i) #posicion del hijo izquierdo
	r = right(i) #posicion del hijo derecho
	if l <= A.heap_size and A[l] >= A[i]
		target = l
	else 
		target = i
	if r <= A.heap_size and A[r] >= A[target]
		target = r
	
	if target =! i
		exchange A[i] con A[target]
		Max_heapify(A, largest)
		
```

Altura del arbol = h
Altura del arbol izq = h-1
Altura del arbol der = h-2

Total: 1 + nodos izq + nodos der

$1 + 2.2^{h-1}-1 + 2^{h-1} -1$
$3.2^{h-1}-1$ cantidad de nodso en el peor caso

T(n) = T($\frac{2}{3}n$) + O(1)

A = 1
B = $\frac{3}{2}$
$f(n) = O(1)$
$n^{\log_{\frac{2}{3}1}}$ $n^0$ = O()1
Caso 2 -> $n^0 \log{n} = \log n$

### Build_max_heap

```python
Build_max_heap(A)
	A.heap_size = A.lenght
	for i = ⌊A.lenght/2⌋ down to 1
		max_heapify(A,i )
```
