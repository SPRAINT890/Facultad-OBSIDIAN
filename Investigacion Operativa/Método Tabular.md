$z = 3x_1 + 5x_2$

#### Funcionales
$x_1 \leqslant 4$
$2x_2 \leqslant 12$
$3x_1 * 2x_2 \leqslant 18$

#### No negatividad
$x_1$, $x_2 \geq 0$


| Original                   | Algebraica               | Variable Basica |
| -------------------------- | ------------------------ | --------------- |
| $z = 3x_1 + 5x_2$          | $z - 3x_1 - 5x_2$        | Z (0)           |
| $x_1 \leqslant 4$          | $x_1 + x_3 = 4$          | $x_3$ (1)       |
| $2x_2 \leqslant 12$        | $2x_2 + x_4 = 12$        | $x_4$ (2)       |
| $3x_1 + 2x_2 \leqslant 18$ | $3x_1 + 2x_2 + x_5 = 18$ | $x_5$ (3)       |

|           |  Z  | $x_1$ |  $x_2$   | $x_3$ | $x_4$ | $x_5$ | LD  |
| :-------: | :-: | :---: | :------: | :---: | :---: | :---: | :-: |
|   Z (0)   |  1  |  -3   | ***-5*** |   0   |   0   |   0   |  0  |
| $x_3$ (1) |  0  |   1   | ***0***  |   1   |   0   |   0   |  4  |
| $x_4$ (2) |  0  |   0   | ***2***  |   0   |   1   |   0   | 12  |
| $x_5$ (3) |  0  |   3   | ***2***  |   0   |   0   |   1   | 18  |
|           |     |       |    *     |       |       |       |     |

##### Columna Pívot

| $x_2$ |
| ----- |
| -5    |
| 0     |
| 2     |
| 2     |

###### Siguiente paso

| Variable Basicas |    Z    |  $x_1$  |    $x_2$    |  $x_3$  |  $x_4$  |  $x_5$  |    LD    |                  |     |
| :--------------: | :-----: | :-----: | :---------: | :-----: | :-----: | :-----: | :------: | ---------------- | --- |
|      Z (0)       |    1    |   -3    |  ***-5***   |    0    |    0    |    0    |    0     |                  |     |
|    $x_3$ (1)     |    0    |    1    |   ***0***   |    1    |    0    |    0    |    4     | $4/0$            |     |
| ***$x_4$ (2)***  | ***0*** | ***0*** | ==***2***== | ***0*** | ***1*** | ***0*** | ***12*** | ***$12/2 = 6$*** | *   |
|    $x_5$ (3)     |    0    |    3    |   ***2***   |    0    |    0    |    1    |    18    | $18/2 = 9$       |     |
|                  |         |         |      *      |         |         |         |          |                  |     |

De la columna pivot divido los numeros por el numero pivot, luego me fijo en los Z si mi numero es negativo entonces agarro el valor absoluto y lo multiplico por la fila pivot y  se la sumo a la fila Z
bajo una fila y como es cero multiplico la fila pivot menos la fila propia

| Variable Basicas | Z   | $x_1$ | $x_2$ | $x_3$ | $x_4$ | $x_5$ | LD  |
| ---------------- | --- | ----- | ----- | ----- | ----- | ----- | --- |
| Z                | 1   | -3    | 0     | 0     | 5/2   | 0     | 30  |
| $x_3$            | 0   | 1     | 0     | 1     | 0     | 0     | 4   |
| $x_2$            | 0   | 0     | 1     | 0     | 1/2   | 0     | 6   |
| $x_5$            | 0   | 3     | 0     | 0     | -1    | 1     | 6   |
|                  | 0   | 0     | 5     | 0     | 5/2   | 0     | 30  |

	Foto 22/8