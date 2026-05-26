

| i   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  | 11  | 12  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| si  | 0   | 1   | 3   | 0   | 5   | 3   | 5   | 6   | 8   | 8   | 2   | 12  | inf |
| fi  | 0   | 4   | 5   | 6   | 7   | 9   | 9   | 10  | 11  | 12  | 14  | 16  | inf |

### PD
AS $[ij]$
			0 Si J=0
			max (AS $[i, k]$ + AS $[k, j]$ + 1)

## Greedy
PG + SO = Spgrande
``ya ordenados tomar el que finaliza antes compatible con las actividades ya elegidas``

soulucion de problema -> si $a_1$ $\in$ As

``` python
Activity_Selector_Recursive(s, f, 0, n)
	Activity_Selector_Recursive(s, f, k, n)
	
```