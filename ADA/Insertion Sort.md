#### El tiempo de ejecucion depende del tamaño del array = n

```Python
## A es un array de 2 elementos
Insertion_Sort(A)
	for i=2  to A.length ## c1(n-1)
		key = A[j] ##c2(n-1)
		i=j-- ##c3(n-1)
		while(i>0 and A[i]>key) ##c4 sum tj
			A[i+1] = A[i] ##c5 sum tj-1
			i=i-- ##c6 sum tj-1
		A[i+1] = key ##c7 (n-1)
```

Tj = la cantidad de veces que itera el while

peor caso TJj = J
mejor caso Tj = 1

suma de los tiempos
c1 . n + c2(n-1) + c3(n-1) + c4 s