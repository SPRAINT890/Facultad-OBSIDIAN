
Dado a $\geq$ 1 y b $\geq$ 1 constante y F(n) una funcion
Sea T(n) definido en los enteros no negativos por la recursion:
	$T(n) = aT(\frac{n}{b}) + f(n)$ con n/b o n/b o n/b

Si $f(n)$ = $O$ ($n^{(\log_ba) - \in}$) para algo $\in$  > 0 -> T(n)= O ($n^{(\log_ba)}$)
Si $f(n)$ = $\theta$ ($n^{(\log_ba)}$) -> T(n) = O (O ($n^{(\log_ba)} \log n$)
Si $f(n)$ = $\Omega$ $(n^{(\log_ba) + \in})$ para algun $\in$  > 0 y si a $f$ n/b $\leq$ cf(n)
					para algun c < 1
						entonces t(n)=O(f(n))
						

$\theta$ es por arriba
$\Omega$ es por abajo

## caso 1
T(n)= 9T$(\frac{n}{3})+n$

a = 9
b = 3
$f$(n) = n

##### calculo del 9T$(\frac{n}{3})$
$\log_3 9 = 2$
por ende pesa $n^2$

si vamos $\in$ = 1
$n^{2-1} = n$


O($n^{2-\in}) = fn$
O(n) = n

## caso 2
T(n) = T$(\frac{2n}{3})+1$

a=1
b=$\frac{3}{2}$                          $\frac{2n}{3} = \frac{n}{\frac{3}{2}}$
$f$n=1

##### Calculo de T$(\frac{2n}{3})$
$\log_{\frac{3}{2}}1 = 0$ 
$n^0$ > $f(n)$

1 y 1 como $f(n) = \theta(n^0)$
###### Solucion
$\log = \theta(\log)$

$n^{\log_{\frac{3}{2}1}}=n^0 = 1$

## Caso 3
T(n) = 3T($\frac{n}{4}+n\log n$)
a = 3
b = 4
$f$n= n log n

##### Calculo de T$(\frac{2n}{3})$

O($n^{\log_4 3}$) = n log n
$n^{0,793}$ = n log n
$n^{0,793+\in}$ = n log n
$\in = 0,2$ -> $n^1$ 

$\Omega(n^1)$ de n log n

## Caso 4 Metodo del arbol
$2T(\frac{n}{2}) + n \log n$
a) 2
b) 2
$f(n) = n \log n$

##### Calculo de $2T(\frac{n}{2})$
$log_2 2 = 1$
$n^{\log_b a}$
n con $n \log n$
$n^{1+\in}$ sigue siendo menor $n \log n$

$\frac{n^{1,1}}{n\log n} = \frac{n^{0,1}}{\log n}$

