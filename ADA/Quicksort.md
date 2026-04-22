
##### Divide $O(n)$ <- Partition() que devuelve la posicion
##### Conquer Recursivo
##### Divide $O(1)$

```python
quicksort(A, p, r)
	if p<r
		q = partition(A, p, r)
		quicksort(A, p, q-1)
		quicksort(A, q+1, r)

partition(A, p, r)
	x = A[r] #1
	i = p-1 #1
	for j = p to r-1 #n
		if A[j] <= x #1
			i = i+1 #1
			swap A[j] with A[i] #1
	swap A[i+1] with A[r] #1
	return i+1 #1
```

#### Invariante
Al principio de cada iteracion, para cada indice del array k y/o x
	Si k esta entre p e i $A[k]$ <= x
	Si k esta entre i e j $A[k]$ > x
	Si k esta en r $A[k]$ = x


#### Coste
T(n) = T(...) + T(...)+ O(n)

T(n) = T(n-1) + T(0) + O(n)
T(n) = T(n-1) + O(n) = $n^2$
