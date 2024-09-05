[[base de datos 2/Practico/Practico 1|Practico 1]]
[[Valor Nulo o NULL|¿Que significa un valor nulo]]
Relacion R (a, b, c, d)
Clave primaria -> a -> {b, c, d}
Clave secundaria -> b -> {a, c, d}

### Atributos Primos
Un atributo primo es un miembro de alguna clave candidata de R

### Dependencia Funcional Total o Parcial
Una dependencia funcional parcial es que un atributo de

## Tabla de forma normal

|                       | Prueba                                                                                                                                                                                          | Remedio (Normalizacion)                                                                                                                                                                                                                         |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1era Forma Normal** | La relacion debe tener atributos multivalor o relaciones anidadas.                                                                                                                              | Generar nuevas relaciones para cada atributo multivalor o relacion anidada                                                                                                                                                                      |
| **2da Forma Normal**  | Para relaciones en las que la clave tenga varios atributos, un atributo no clave debe depender parcialmente de la clave primaria                                                                | Descomponer y configurar una nueva relacion por cada clave parcial con sus atributos dependientes.<br>Asegurar de mantener una relacion con la clave principal original y cualquier atributo que sea funcionalmente dependiente (total) de ella |
| **3era Forma Normal** | La relacion tiene un atributo no clave que esta funcionalmente determinado por otro atributo no clave.<br>Es decir, hay una dependencia transitiva de un atributo no clave de la clave primaria | Descomponer y configurar una relacion que incluya el(los) atributo(s) no clave que determine(n) funcionalmente otro(s) atributo(s) no clave.                                                                                                    |


### Primera forma Normal
1. El dominio de un atributo solo debe incluir valores atómicos (simples, indivisibles)
2. Los atributos no pueden ser multivaluados ni compuestos
3. Prohíbe las relaciones dentro de las relaciones o las relaciones como valores de atributos dentro de las tuplas

![[Pasted image 20240808200924.png]]
En este caso se tiene que hacer una tabla Ubicacion, con NroDepto y Ubicacion como clave primaria

### Segunda forma Normal
Un esquema de relacion R esta en segunda forma normal si todo atributo no primo A en R es completa y funcionalmente dependiente de la clave principal R
![[Pasted image 20240820201845.png]]Ejemplo de por que no tener todo en una tabla


| DNI | Numproy | Horas | NombreEmpl | NombreProy | UbicacionProy |
| --- | ------- | ----- | ---------- | ---------- | ------------- |
| 1   | P1      | 10    | Seba       | B2         | Mdeo          |
| 1   | P2      | 5     | Seba       | B1         | Mdeo          |
| 2   | P1      | 10    | Juan       | B2         | Mdeo          |

Se duplican datos y en caso de querer cambiar un dato, puede haber inconsistencia en la base de datos

### 3era Forma Normal
Un esquema de relación R está en Tercera Forma Normal si cumple la segunda forma normal y ningún atributo no primo A en R es transitivamente dependiente de la clave principal de R

![[Pasted image 20240820205235.png]]


### Forma normal de BCNF (Boyce-Codd)

![[Pasted image 20240820210702.png]]