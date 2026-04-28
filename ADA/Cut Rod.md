Mayor ingreso posible a partir de la varilla?

|        | 1   | 2   | 3   | ... | n   |
| ------ | --- | --- | --- | --- | --- |
| precio |     |     | 10  |     | 25  |

S(n) => Max(S(1)+S(5), S(2)+S(4), S(3)+S(3), S(4)+S(2), S(5)+ S(1))
S(n) = Max(P(n), S(1) + S(n-1), S(2)+S(1-2) ... S(n-1)+ S(1))

tambien podemos decir de cuanto queremos el primer corte y calcular a partir del resto

P(1) + S(5)
P(2) + S(4)
P(3) + S(3)
P(4) + S(2)
P(5) + S(1)

S(n) = Max($P_i$ + S(n - i))
