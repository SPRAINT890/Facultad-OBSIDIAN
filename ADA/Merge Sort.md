paradigma divide and conquer

Divide: dividir en problema mas chico
Conquer: resolver el problema mas chico
Combine: combinar esas soluciones

#### Merge Sort
T(n): 1- O(1) si n=1
     2- O(divide) + O(conquer) + O(combine) si n>1
        O(1) + 2T($\frac{n}{2}$) + O(n)

```python
Merge_Sort(A, p, r)
	if(p<r):
		q=(p+r)/2
		Merge_Sort(A,p, q)
		Merge_Sort(A,q+1, p)
		Merge(A, p, q, r)
	
```

![[Pasted image 20260324200425.png |350]]

#### Merge

```python
merge(A, p, q, r)

```