## Extreme Programming (XP)
- Desarrollo iterativo a niveles “extremos” (Kent Beck, 1998) 
- Liberaciones muy frecuentes y en paralelo 
- Integración continua/entrega continua (CI/CD) 
- Historias de usuario (requisitos) 
- Programación en pares (pair programming) 
	- Propiedad colectiva del código del sistema
- Desarrollo dirigido por pruebas (TDD Test Driven Development) 
	- Programar primero los unit test y luego el programa
	- Puede que los unit test esten sesgados
- Alto involucramiento del cliente 
- Simplicidad y refactorización (refactoring) constantes

### TDD
- Enfoque para abordar pruebas (verificación) sin especificación
- Se diseñan y desarrollan las pruebas antes de implementar 
- Desarrollo de pruebas incremental basado en HU 
- El cliente participa en el desarrollo y validación de la prueba 
- Basado en la automatización 
- Puedo ejecutar la prueba durante el desarrollo, para descubrir los problemas antes

### Refactorizar
- Anticiparse a los cambios futuros es costoso 
- El equipo de desarrollo busca posibles mejoras en el software y los implementa de inmediato 
	- Si ve una posible mejora, la realiza 
- Permite mejorar la estructura y legibilidad del software 
- El software siempre debe ser fácil de entender y cambiar a medida que se proponen nuevos requisitos.
- es buena practica generar un sprint para mejorar el producto

## Scrum
Marco de trabajo liviano que ayuda a las personas, equipos y organizaciones a generar valor a través de soluciones adaptativas para problemas complejos. 
- Se basa en el empirismo y el pensamiento Lean. 
	- El conocimiento proviene de la experiencia y de la toma de decisiones con base en lo observado. 
	- Reducir el desperdicio y enfocarse en lo esencial
- Respeta el manifiesto ágil -> Metodología ágil 
- Se centra en la gestión ágil de proyectos 
- No plantea el uso de ninguna técnica específica
- Se puede utilizar en otros tipos de negocios

[[Sprint|¿Que es un sprint?]]
### Equipo (scrum team)
![[Pasted image 20240903182958.png]]

#### Product Owner
- Promueve maximizar el valor del producto
- Gestiona el Product Backlog 
	- Desarrollar y comunicar explícitamente el Objetivo del Producto 
	- Crear y comunicar claramente los elementos del Product Backlog 
	- Ordenar los elementos del Product Backlog 
	- Asegurarse de que el Product Backlog sea transparente, visible y se entienda 
- Puede representar las necesidades de muchos interesados (stakeholders) en el Product Backlog

#### Scrum Master
- Responsable de transmitir al Scrum Team la teoría y práctica de Scrum 
- Apoya al Scrum Team en sus actividades scrum (facilitador) 
- Promueve que el equipo se autogestionado y multifuncional 
- Ayudar al Scrum Team a enfocarse en crear incrementos de valor que cumplan con la Definición de Terminado 
- Asegurarse de que todos los eventos de Scrum se lleven a cabo y sean positivos, productivos y se mantengan dentro de los límites de tiempo recomendados.

#### Developers
- Responsables del incremento 
- Responsables de crear un plan para el Sprint (Sprint Backlog) 
- Definen la calidad a través Definición de Terminado definition of done (DoD)

##### Definition of Done (DoD)
Que es necesario que tenga una historia de usuario para que se considere que esta hecho
ejemplos:
- Test unitario
- Documentación


### Artefactos
#### Product Backlog PB
- Lista ordenada de lo que es necesario hacer para alcanzar el objetivo del producto

#### Sprint Backlog SB
- Contiene 
	- objetivo del Sprint (por qué) 
	- elementos del PB (qué)
	- plan de acción (cómo)
#### Incremento
- Tiene que cumplir con el DoD 
- Debe ser utilizable

#### Ceremonias
##### Sprint
- Contiene todos los eventos 
- Duración fija 
- Se persigue en todo momento el Objetivo del Sprint.
##### Sprint Planning
- Inicia el Sprint 
- Se define Objetivo del Sprint, se seleccionan elementos del PB y se define plan de acción. 
	- 8hs (sprint 4 s)
##### Daily Scrum
- Chequea el progreso hacia el objetivo del sprint 
- 15’ Devolopers
#### Sprint Review
- Revisar el resultado del Sprint 
	- 4hs (sprint 4 s)
#### Sprint Restrospective
- Planificar cómo mejorar (calidad y la efectividad) 
- Finaliza el Sprint 
- 3hs (sprint 4 semanas)

