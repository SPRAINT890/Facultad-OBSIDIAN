
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
	
	nm if target =! i
		exchange A[i] con A[target]
		Max_heapify(A, largest)
		
```