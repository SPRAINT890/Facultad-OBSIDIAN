## Resumen
- Que es el software
- que es la ing de software
- etapas del software
- modelo de procesos


## Requisito == Requerimiento
Descripcion de lo que el sistema debe hacer: el servicio que ofrece y las restricciones en su operacion.

==ES ESPECIFICAMENTE QUE QUIERE EL CLIENTE O QUE SE DEBE HACER, LO CUAL ES DISTINTO AL COMO==

## Costos de errores en los requisitos
Fases del desarrollo

| Especificacion de software | Desarrollo de software | Verificacion y validacion de software | Evolucion del software |
| :------------------------: | :--------------------: | :-----------------------------------: | :--------------------: |
|             +              |           ++           |                  +++                  |          ++++          |
Es mucho mas costoso arreglar algo al final que al inicio

## Niveles de descripcion (Abstraccion)
- De usuario
	- Lenguaje natural
	- diagramas de los servicios que brinda
	- limitaciones operativas
	- Escrito para los clientes
- Del Sistema
	- Documento estructurado (especificacion funcional)
	- Descripciones detalladas de funciones, servicios y restricciones operativas
	- Lo que se debe implementar

### Ejemplo de usuario
El sistema Mentcare generará informes de gestión mensuales que permitan visualizar el costo de los medicamentos prescritos por cada clínica durante el mes

### Ejemplo de Sistema
1.1 El último día hábil de cada mes, se generará un resumen de los medicamentos recetados, su costo y las clínicas que los recetaron. 

1.2 El sistema generará el informe para imprimirlo después de las 17.30 horas del último día hábil del mes. 

1.3 Se creará un informe para cada clínica y se enumerarán los nombres de los medicamentos, el nro, total de recetas, el nro, de dosis recetadas y el costo total de los medicamentos recetados. 

1.4 Si los medicamentos están disponibles en diferentes unidades de dosis (por ejemplo, 10 mg, 20 mg, etc.), se crearán informes separados para cada unidad de dosis. 

1.5 El acceso a los informes de costos de los medicamentos estará restringido a los usuarios autorizados que figuren en una lista de control de acceso de administración.

## Tipos de requisitos
### Funcionales
Que tiene que hacer el sistema, como tiene que responde en ciertos contextos y que debe hacer.
Es la funcionalidad que hay del sistema.
Ejemplo Instagram:
Subir una foto, comentar, etc
- Se pueden describir en usuario y/o sistema
- como deberia ser la especificacion?
	- Completa: deben definirse todos los servicios requeridos
	- Consistente (Coherente): Evitar definiciones contradictorias

### No funcionales
Restricciones de las funciones o servicios, limitaciones de tiempo, limitaciones al proceso de desarrollo y limitaciones impuestas por las normas
Aplican al sistema en su conjunto en lugar de a características o servicios individuales del sistema
Ejemplo Instagram:
Donde se guardan los datos, tolerancia a fallas, etc
tipos:
- Del producto
- Organizacionales
- Externos


| Producto                                                                                                                                                                                                             | Organizacionales                                                                        | Externos                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Especifican o limitan el comportamiento del software.                                                                                                                                                                | Responden a políticas o procedimientos organizacionales                                 | Responden a factores externos al sistema y organizacion                                                                               |
| - Mentcare estará disponible para todas las clínicas durante el horario laboral normal (L-V, de 08:30 a 17:30) <br>- El tiempo de inactividad dentro del horario laboral normal no excederá los 5 segundos en un día | - Los usuarios de Mentcare deberá autenticarse con identidad digital de Abitab o Antel. | - El sistema implementará disposiciones de privacidad de datos dispuestos en la Ley N° 18331, “Ley de Protección de datos personales” |

![[Pasted image 20240820184142.png]]

## Cuantificar Req No Funcionales
PROBLEMA: cuando los declaro, los declaro como un objetivo generla "alto nivel"


| Quiero que mi sistema sea rapido  | - Transacciones/Segundos<br>- Tiempo de respuesta                             |
| --------------------------------- | ----------------------------------------------------------------------------- |
| **Quiero que mi sistema sea robusto** | **- Porcentaje de fallas en un periodo<br>- Tiempo de reinicio despues de falla** |


## Proceso de software: Actividades
![[Pasted image 20240820185447.png]]


## Especificación de software / Requisitos de software

![[Pasted image 20240820185849.png]]

### Adquisición y análisis
Proceso en el cual se trabaja con clientes, usuarios finales, interesados para descubrir dominio de aplicación, qué servicios debe proporcionar el sistema, restricciones, etc.
Hay una etapa de interiorización del dominio que se va a trabajar.

![[Pasted image 20240820190529.png]]


### Analisis de interesados

![[Pasted image 20240820190600.png]]


### ¿Que desafios/problemas me puedo encontrar cuando obtenemos y analizamos requisitos?
- No este claro
- No sea factible
- Muchos sistemas
	- Sistemas grandes
	- Critico
- Dominio
- Muchos interesados con diferentes necesidades

### Ciclo de Obtención y Análisis de requisitos
![[Pasted image 20240820191327.png]]


### Descubrir y comprender requisitos
- Identificar fuentes de información 
- Interactuar con los interesados (stakeholders) 
- Identificar requisitos del dominio y reglas de negocio 
- Ambiente organizacional y operacional 
- Organizar y agrupar la información los interesados 
	- Considero cada grupo de interesados como un punto de vista y obtengo todos los requisitos de ese grupo en el punto de vista.

### ¿Cómo relevan o revelarían requerimientos? ¿Por que usan o utilizarían ese método?
- Preguntando
- Estudio de mercado
- Cuestionarios
- Experiencia
- Cambio de perspectiva con el cliente
- Mostrar similar
- Entrevistas
- Talleres/Laboratorios(Workshops)
- Etnografías (Observación)

#### Entrevistas
- Tipos
	- Cerradas: responde a un conjunto de preguntas predefinidas
	- Abiertas: no existe una agenda previa de pregunta, se exploran requerimientos
- Es dificil relevar requerimientos o restricciones del dominio
	- Lenguaje, conceptos del dominio especifico
	- Se dan por hecho conocimientos previos
- Es dificil relevar requisitos o restricciones organizacionales

Cualidades del entrevistador: