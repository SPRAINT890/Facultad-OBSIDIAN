### [[Requisitos |Requisitos del software]]
### Actividades involucradas en la producción de software
1. Relevar
	- Mercado
	- Necesidades
	- Alcance
2. Diseño
3. Programar
4. Testing
5. Evolución/Mantenimiento

### Tipos de procesos de software
- Plan-drive(Dirigidos por planes o tradicionales):
	- Toda actividad debe ser planeada con aticipacion
	- El progreso (avance) se mide con respecto al plan inicial

- Agile(Agiles cap 3) 
	- La planificacion es incremental (por fases)

### Modelos de procesos
- Son una representacion simplificada del proceso (abstraccion)
- Marcos (Frameworks) adaptables

#### Cascada
Son etapas que inician cuando la anterior etapa inicia, y finalizan para darle comienzo a otra, no se puede iniciar una etapa sin antes finalizar otra, son dificiles de volver atras, el cliente no tiene contacto de inicio a fin del proceso.

#### Dirigidos por planes o incremental
modelo donde se le va entregando al cliente distintas versiones del producto, que sea usable para el cliente, para que pueda validar

#### Integración y configuración (Reutilización)
partiendo de una especificación de requerimientos, pasando por un descubrimiento de software, pasando despues por el refinamiento de proceso.


### Cascada vs Incremental
#### Positivo Cascada
- Es mejor porque no se ve al cliente para el proceso, pero no para el producto
- Requisito claros que no cambien
- Es organizado
- Mas documentación
En general es mejor para un sistema grande, sistemas críticos (MS)
#### Negativo Cascada
- Menor adaptabilidad
- No ver el cliente
- Menos Flexible, Requerimientos, Procesos o etapas
- No se ven avances
- Puede que el producto sea obsoleto por que no lo aprueba el cliente
- Riesgo de errores de etapas
- Atraso fase a fase
Tiempo de mercado rápidos, Requisitos incrementales

#### Positivo Incremental
- Ajustes mas tempranos y mas flexible
- Adapto al cliente
- Cliente evalua sobre las demos
- El cliente puede evaluar el producto en la etapa de desarrollo, generando una comentario
- El cliente puede cambiar los requerimientos, eso hace que se adaptable a cambios
- El cliente al tener distintas versiones funcionales del producto, puede empezar a darle valor al software
- Es organizado
- comunicación clara con el cliente
Proyectos Chicos o de menor coste, proyectos de requerimientos cambiantes, app web

#### Negativo Incremental
- No es visible proceso, ¿Cómo avanzo?
- Entregas en poco tiempo
- a veces los productos se desarrollan rápido y no da tiempo a documentarlo
- el cambio regular tiende a corromper su estructura. haciendo que la incorporación de más cambios de software se vuelve cada vez más difícil y costosa.

## Errores de software

### Errores
Accion humana que produce un resultado incorrecto, genera el defecto

### Defectos (Bug)
Manifestacion de ese error en el codigo

### Falla
Revelacion del bug al utilizar el sistema, en tiempo de ejecucion
- No hace lo que se esperaba
- Hace algo que no se esperaba
- No responde en los tiempos esperados
#### Sucede por que puede haber errores en las fases del desarrollo

### Testear vs Debuggear
- Detectar (Mas o menos sistematica) fallas (que indican la presencia de defectos)
- Objetivos testear
	- Ejecutar un programa para encontrar fallas
	- Ejecutar un programa para medir la calidad 
	- Ejecutar un programa para brindar confianza 
	- Analizar un programa o su documentación para prevenir fallas
- Objetivo debuggear
	- Localizar y corregir fallas

### Terminologia
Caso de prueba ○ Conjunto detallado de condiciones, acciones y resultados esperados. ○ Objetivo de prueba, pre y pos condiciones, pasos, datos de prueba, resultados esperados, estado ● Objetivo de la prueba/tipo de prueba (est objective/test type) ○ Propósito de la prueba, ¿Qué quiero probar? ● Técnica de prueba ○ Técnica o estrategia utilizada para especificar o ejecutar la prueba. ● Objeto de prueba ○ Objeto de prueba que se va a probar ● Nivel de prueba: ○ Nivel de acuerdo al modelo de ciclo de vida (unitarias, integración, sistema) ● Grado de prueba ○ Nivel de exhaustividad con el que se realiza el proceso de pruebas en un sistema o aplicación de software (básico, medio, exhaustivas)