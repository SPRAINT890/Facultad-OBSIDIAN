paradigma divide and conquer

Divide: dividir en problema mas chico
Conquer: resolver el problema mas chico
Combine: combinar esas soluciones

```python
Merge_Sort(A, p, r)
	if(p<r):
		q=(p+r)/2
		Merge_Sort(A,p, q)
		Merge_Sort(A,q+1, p)
		Merge(A,p, q)
	
```

![[Pasted image 20260324200425.png |350]]