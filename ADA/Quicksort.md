
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
	x = A[r]
	i = p-1
	for j = p to r-1
		if A[j] <= x
			i = i+1
			swap A[j] with A[i]
	swap A[i+1] with A[r]
	return i+1
```

#### Invariante
Al principio de cada iteracion, para cada indice del array k y/o x
	Si k esta entre p e i $A[k]$ <= x
	Si k esta entre i e j $A[k]$ > x
	Si k esta en r $A[k]$ = x