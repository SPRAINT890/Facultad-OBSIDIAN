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
R (dni, num_proy, nom_empl, salario, telef_e)





