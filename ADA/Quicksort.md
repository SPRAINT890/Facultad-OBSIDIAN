
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
```
