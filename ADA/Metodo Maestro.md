
Dado a $\geq$ 1 y b $\geq$ 1 constante y F(n) una funcion
Sea T(n) definido en los enteros no negativos por la recursion:
	$T(n) = aT(\frac{n}{b}) + f(n)$ con n/b o n/b o n/b

Si $f(n)$ = O($n^{(\log_ba) - \in}$) para algo $\in$  > 0 -> T(n)= O ($n^{(\log_ba)}$)
Si $f(n)$ = O ($n^{(\log_ba)}$) -> T(n) = O (O ($n^{(\log_ba)} \log n$)
Si $f(n)$ = $\Omega(n^{(\log_ba) - \in})$ para algun $\in$  > 0 y si a $f$ n/b $\leq$ cf(n)
					para algun c 
						entonces t(n)=O(f(n))
						


## ejemplo
T(n)= 9T($\frac{n}{3}+n$)

a = 9
b = 3
$f$(n) = n

O($n^{2-\in}) = fn$
O(n) = n