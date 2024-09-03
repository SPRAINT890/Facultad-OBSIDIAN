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
- El Product Backlog es una lista emergente y ordenada de lo que se necesita para mejorar el producto. 
- Es la única fuente del trabajo realizado por el Scrum Team. 
- El refinamiento del Product Backlog es el acto de dividir y definir aún más los elementos del Product Backlog en elementos más pequeños y precisos. 
- Objetivo del Producto 
	- Describe un estado futuro del producto que puede servir como un objetivo para que el Scrum Team planifique.
#### Sprint Backlog SB
- Contiene 
	- objetivo del Sprint (por qué) 
	- elementos del PB (qué)
	- plan de acción (cómo)
- Objetivo del Sprint (por qué)
- Conjunto de elementos del Product Backlog seleccionados para el Sprint (qué), así como un plan de acción para entregar el incremento (cómo). 
- Está gestionado por los Developers 
- Foto en tiempo real del trabajo que los Developers 
- Se actualiza a lo largo del Sprint a medida que se aprende más. Debe tener suficientes detalles para que puedan inspeccionar su progreso en la Daily Scrum.
#### Incremento
- Tiene que cumplir con el DoD 
- Debe ser utilizable
- “Parte de software utilizable”. hacia el Objetivo del Producto.
- Cada incremento se suma a todos anteriores y se verifica 
- Es posible crear más de 1 incremento por sprint 
- La suma de los Increments se presenta en la Sprint Review 
- Se puede entregar un Increment a los interesados antes del final del Sprint. 
- Todo lo que forma parte de un incremento cumple con la Definición de Terminado (Definition of Done, DoD)

#### Ceremonias
##### Sprint
- Contiene todos los eventos 
- Duración fija 
- Se persigue en todo momento el Objetivo del Sprint.
- Eventos de duración fija de (=< 1 mes) 
- Cada sprint inmediatamente después del cierre del sprint anterior 
- Sprint Planning, Daily Scrums, Sprint Review y Sprint Retrospective son parte del sprint 
- Durante el Sprint: 
	- No se realizan cambios que pongan en peligro el Objetivo del Sprint 
	- El Product Backlog se refina según sea necesario; 
	- El alcance se puede aclarar y re negociar con el Product Owner a medida que se aprende
- Puede cancelarse si el Objetivo del Sprint se vuelve obsoleto. Solo el Product Owner tiene la autoridad para cancelar el Sprint.
##### Sprint Planning
- Inicia el Sprint 
- Se define Objetivo del Sprint, se seleccionan elementos del PB y se define plan de acción. 
	- 8hs (sprint 4 s)
- Da inicio al Sprint 
- Se define trabajo que se realizará para el Sprint. 
- El Scrum Team también puede invitar a otras personas a asistir a la Sprint Planning para brindar asesoramiento. 
- Pasos 
	- Objetivo del sprint: ¿Por qué es valioso este Sprint? 
	- ¿Qué se puede hacer? 
	- ¿Cómo se puede hacer?
##### Daily Scrum
- Chequea el progreso hacia el objetivo del sprint 
- 15’ Devolopers
- Inspeccionar el progreso hacia el Objetivo del Sprint 
- Evento de 15 minutos para los Developers del Scrum Team. 
- Se desarrolla a la misma hora y en el mismo lugar todos los días hábiles 
- Si el Product Owner o Scrum Master están trabajando activamente en elementos del Sprint Backlog, participan como Developers. 
- Mejora la comunicación, se identifican impedimentos, promueven la toma rápida de decisiones y, en consecuencia, eliminan la necesidad de otras reuniones.
#### Sprint Review
- Revisar el resultado del Sprint 
	- 4hs (sprint 4 s)
- Sesión de trabajo para inspeccionar el resultado del Sprint y determinar futuras adaptaciones. 
- Scrum Team presenta los resultados de su trabajo a los interesados clave 
- Se discute el progreso hacia el Objetivo del Producto 
- Se identifican siguientes pasos 
- El Product Backlog también se puede ajustar para satisfacer nuevas oportunidades.
#### Sprint Restrospective
- Planificar cómo mejorar (calidad y la efectividad) 
- Finaliza el Sprint 
- 3hs (sprint 4 semanas)
- Planificar formas de aumentar la calidad y la efectividad. 
- El Scrum Team inspecciona cómo fue el último Sprint con respecto a las personas, las interacciones, los procesos, las herramientas y su DoD 
- El Scrum Team analiza qué salió bien durante el Sprint, qué problemas encontró y cómo se resolvieron (o no) esos problemas. 
- El Scrum Team identifica los cambios más útiles para mejorar su efectividad. 
- Las mejoras se aplican lo antes posible (se pueden agregar al Sprint Backlog para el próximo Sprint) 
- La Sprint Retrospective finaliza el Sprint


