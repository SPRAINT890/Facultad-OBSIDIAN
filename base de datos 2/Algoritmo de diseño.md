Dado F, G es la cobertura mínima de F

- $G^+ = F^+$
- En G, todas las DF están expresadas en forma canónica $X \rightarrow Y$, donde Y tiene un solo atributo
- Para todas las DF, si elimino un atributo de X, la DF deja de ser valida
- Si elimino una DF de G, se deja de cumplir $G^+ = F^+$

Cuando se hace una descomposición no queremos perder atributos ni dependencias funcionales

## Conservación de dependencias
Dado un conjunto de dependencias F en R, la proyección de F en $R_i, \pi R_iF$, Donde $R_i$ es un subconjunto de R, es el conjunto de dependencias $X \rightarrow Y$ en $F^+$ tales que los atributos X U Y se encuentran todos en $R^i$

Relacion Universal: R ($A_1, A_2, ..., A_n$)
Conjunto DF: F = {$DF_1, DF_2, ..., DF_m$}
Descomposición: D = {$R_1, R_2, ..., R_e$}

R(DNI, Nombre, Apellido, IdProyecto, NombreProyecto)
F: {$DNI \rightarrow nombre, apellido$}
	{$IdProyecto \rightarrow NombreProyecto$}
D = {$R_1, R_2$} $R_1$ (DNI, nombre, apellido)
			$R_2$ (IdProyecto, NombreProyecto)

- Se conservan atributos
- Se conservan DF


##### Relacion Universal:
R (dni, num_proy, nom_empl, salario, telef_empl, num_depto, nom_proy, ubic_proy)

##### Dependencias Funcionales
dni $\rightarrow$ salario, telef_empl, num_depto
num_proy $\rightarrow$ nom_proy, ubic_proy
dni, num_proy $\rightarrow$ salario, telef_empl, num_depto, nom_proy, ubic_proy

## Concatenacion (Join) sin perdida
Una descomposición D = ($R_1, R_2, ..., R_m$) de R, cumple con la propiedad de concatenación sin pérdida respecto al conjunto de dependencias funcionales F en R, si para cada estado de relación r de R que satisface F, se mantiene lo siguiente:
![[Pasted image 20240827204935.png | 500]]

==La propiedad de concatenación sin pérdida garantiza que no se generarán tuplas falsas cuando se aplica un join a las relaciones de la descomposición.==


#### R

| CI  | Nombre | Apellido | IdP | NombreProyecto |
| --- | ------ | -------- | --- | -------------- |
| 1   | Seba   | Garcia   | 2   | BD 2           |
| 2   | Diego  | Lopez    | 2   | BD 2           |
| 3   | Analia | Conde    | 1   | BD 1           |

#### $R_1$

| CI  | Nombre | Apellido | IdP |
| --- | ------ | -------- | --- |
| 1   | Seba   | Garcia   | 2   |
| 2   | Diego  | Lopez    | 2   |
| 3   | Analia | Conde    | 1   |

#### $R_2$


| IdP | NombreProyecto |
| --- | -------------- |
| 1   | BD 1           |
| 2   | BD 2           |

- $R_1 \cap R_2 \rightarrow$ ($R_1$)


