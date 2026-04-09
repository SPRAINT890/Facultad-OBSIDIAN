![[Pasted image 20260409183011.png]]

$\log^4{n} = i$
cantidad de niveles log n +1

nodos por nivel $3^i$
costo por nivel = $3^i(\frac{n}{4})^2$


### parte 2

Tn = T$(\frac{n}{3})$ + T($\frac{2n}{3}$) + cn

![[Pasted image 20260409185629.png]]

![[Pasted image 20260409190839.png]]
pero uno de las fracciones llega antes a O(1), por ende decimo que todos los niveles valen cn

$(\frac{2}{3})^in=1$
$n = (\frac{3}{2})^i$
$i = \log_{\frac{2}{3}}{n}$

esto da un aproximado, para saber el valor exacto debo utilizar sustitucion

$Cn(\log_{\frac{2}{3}}{n+1}) =$ O(        )
$Cn(\log_{\frac{2}{3}}{n+1}) = Cn \log_{\frac{2}{3}}n+Cn =$ O ($n\log n$)
