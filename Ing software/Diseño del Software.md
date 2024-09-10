...

...

## Patrones
Describe una estructura de diseño que resuelve un problema particular del diseño dentro de un contexto específico.
Si hay un software que soluciona parcialmente mi problema lo utilizo, analizo los patrones y luego los utilizo
## Divide and Conquer
- Es más fácil sencillo resolver un un problema complejo si se divide en elementos manejables. 
- En general, cuando se combinan dos problemas, la complejidad es mayor que la suma de la complejidad tomada por separado.


## Modularización
- Dividir en una serie de componentes “más pequeños”, con interfaces bien definidas que describen las interacciones de los componentes. 
- Un sistema es modular si está formado por un conjunto de componentes que se pueden implementar separadamente y el cambio en un componente tiene mínimos impactos en otros componentes 
- Colocar diferentes funcionalidades y responsabilidades en diferentes componentes
- Single responsibility (SRP) 
	- Cada componente/módulo debe ser responsable de una sola funcionalidad ● Promueve la modularidad 
- Minimiza el impacto de un cambio 
- ¿DESVENTAJAS?
	- La contra es que se podría hacer un modulo por función, saturando la comunicación de los módulos

![[Pasted image 20240910182122.png]]

## Encapsular
- Agrupar y empaquetar los detalles internos de una abstracción 
- Los detalles son inaccesibles para las entidades externas. 
- La modularidad efectiva se logra definiendo un conjunto de módulos independientes que intercambien sólo la información necesaria para lograr la función del software en su totalidad.
- Lo que me interesa son que interfaces tiene, mas que como se implementa.

## Independencia Funcional
- ACOPLAMIENTO 
	- Media que indica la dependencia relativa entre componentes 
	- Si tengo un alto acoplamiento, entonces es más difícil comprender y modificar, por ende es mejor tenerlo en el mismo modulo
- COHESIÓN 
	- Medida que indica la fortaleza funcional de un módulo/componente 
	- Si tengo una alta cohesión es más sencillo de comprender y modificar el módulo

## Re-uso
- “NO REINVENTAR LA RUEDA” 
- Niveles 
	- De abstracción: reutiliza el conocimiento de abstracciones exitosas en el diseño. 
	- Objeto: reutiliza objetos disponibles en lugar de escribir el código nuevamente 
	- Componentes: reutiliza colecciones de objetos 
	- Nivel del sistema: reutiliza sistemas de aplicación completos

### Ventajas
- Si el software ha sido verificado y utilizado en producción, es más confiable que el software nuevo 
- Conozco el costo del software 
- Acelera tiempos de desarrollo
### Desventajas
- Difícil de mantener
- Existe documentación necesaria? 
- Síndrome de “no esta inventado aquí”

# [[Principio de Diseño]]
