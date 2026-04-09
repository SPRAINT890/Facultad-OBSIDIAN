
Dado a $\geq$ 1 y b $\geq$ 1 constante y F(n) una funcion
Sea T(n) definido en los enteros no negativos por la recursion:
	$T(n) = aT(\frac{n}{b}) + f(n)$ con n/b o n/b o n/b

Si $f(n)$ = O($n^{(\log_ba) - \in}$) para algo $\in$  > 0 -> T(n)= O ($n^{(\log_ba)}$)
Si $f(n)$ = O ($n^{(\log_ba)}$) -> T(n) = O (O ($n^{(\log_ba)} \log n$)
Si $f(n)$ = $\Omega(n^{(\log_ba) + \in})$ para algun $\in$  > 0 y si a $f$ n/b $\leq$ cf(n)
					para algun c 
						entonces t(n)=O(f(n))
						


## ejemplo 1
T(n)= 9T($\frac{n}{3}+n$)

a = 9
b = 3
$f$(n) = n

O($n^{2-\in}) = fn$
O(n) = n

## ejemplo 2
T(n) = T($\frac{2n}{3}+1$)

a=1
b=$\frac{3}{2}$                          $\frac{2n}{3} = \frac{n}{\frac{3}{2}}$
$f$n=1


$n^{\log_{\frac{3}{2}1}}=n^0 = 1$

## ejemplo 3
T(n) = 3T($\frac{n}{4}+n\log n$)
a = 3
b = 4
$f$n= n log n

O($n^{\log_4 3}$) = n log n
$n^{0,793}$ = n log n
$n^{0,793+\in}$ = n log n
$\in = 0,2$ -> $n^1$ 

$\Omega(n^1)$ de n log n