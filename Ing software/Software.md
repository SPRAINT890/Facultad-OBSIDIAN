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
- Caso de prueba 
	- Conjunto detallado de condiciones, acciones y resultados esperados. 
	- Objetivo de prueba, pre y pos condiciones, pasos, datos de prueba, resultados esperados, estado 
- Objetivo de la prueba/tipo de prueba (est objective/test type) 
	- Propósito de la prueba, ¿Qué quiero probar? 
- Técnica de prueba 
	- Técnica o estrategia utilizada para especificar o ejecutar la prueba. 
- Objeto de prueba 
	- Objeto de prueba que se va a probar 
- Nivel de prueba: 
	- Nivel de acuerdo al modelo de ciclo de vida (unitarias, integración, sistema) 
- Grado de prueba 
	- Nivel de exhaustividad con el que se realiza el proceso de pruebas en un sistema o aplicación de software (básico, medio, exhaustivas)

## ¿Qué hacemos cuando probamos software?
Los procesos de verificación y validación (V&V) buscan comprobar que el software cumple con sus especificaciones, y brinda las funcionalidades deseada por los clientes. 
- Verificar 
	- ¿Construimos bien el producto?
- Validar 
	- ¿Construimos el producto correcto?
- Los procesos de V&V comienzan tan pronto como están disponibles los requerimientos y continúan a través de todas las etapas del proceso de desarrollo.

## Niveles de confianza
Los procesos V&V buscan establecer confianza de que el sistema de software es “adecuado”. 
- Propósito del software 
	- Más crítico -> Más confiabilidad 
- Expectativas del usuario 
	- Los beneficios del uso deben exceden los costos de la recuperación de fallas 
- Entorno de mercado 
	- Productos competitivos, menos calidad, menos precio

#### Deuda técnica
![[Pasted image 20241015183134.png | 200]]
Son cosas que dejo para despues por tiempo o dinero, que se van sumando y acorta el alcance

### ¿Es posible garantizar que un software NO tiene defectos y que se comporta como se espera? 
Las pruebas sólo pueden mostrar la presencia de errores, pero NO su ausencia

## Principios de VyV
-  Sirve para revelar defectos, pero no su ausencia 
- No es posible ser exhaustivos 
- Las actividades deberían comenzar lo antes posible 
- Agrupación de defectos (defect clustering) 
	- arreglando el 20% de los errores, solucionas el 80 % de los problemas
- La paradoja del pesticida 
- En necesario tener en cuenta el contexto-dependiente 
- No existe el software sin fallas

## Etapas finales de un programa o un ciclo
![[Pasted image 20241015184204.png]]
### De desarrollo
- #### Unitarias (de módulo o componente) 
	- Unidades individuales o clases de objetos 
	- Probar la funcionalidad de objetos o métodos. 
	- Objetivo de prueba: 
		- Verificar componente o módulo de un software de acuerdo a su especificación técnica 
	- Objeto: 
		- Clases, módulos, etc. 
	- Entorno: 
		- Ambiente de desarrollo 
	- Se basa en la lógica de procesamiento interno y de las estructuras de datos dentro de las fronteras de un componente 
	- Puede requerir construir drivers (pruebas de integración ascendentes) y stubs (pruebas de integración descendentes)
	- Siempre que sea posible, se debe automatizar las pruebas unitarias 
	- Seleccionar casos de prueba unitarios eficaces 
		- Deben mostrar que, cuando se utilizan como se espera, el componente hace lo que se supone que debe hacer. 
		- Si existen defectos en el componente, estos deben revelarse

- De componentes (de integración) 
	- Integran varias unidades individuales, componentes compuestos 
	- Probar las interfaces de los componentes 
- Del Sistema 
	- Integran algunos o todos los componentes de un sistema y se prueba el sistema en su totalidad 
	- Interacciones entre componentes

### Técnicas de pruebas
- Pruebas de partición 
	- Identificar grupos de entradas que tienen características comunes y que deben procesarse de la misma manera. 
	- Grupos (dominos) de entradas y salidas con características comunes 
- Basadas en pautas 
	- Utilizar pautas de prueba para elegir casos de prueba 
	- Las pautas reflejan experiencia previa de los tipos de errores comunes
#### Pruebas de partición 
Función que valida contraseñas bajo los siguientes criterios: 
- La contraseña debe tener al menos 8 caracteres. 
- Debe contener al menos una letra mayúscula. 
- Debe contener al menos un número. 
- Debe contener al menos un carácter especial (por ejemplo, @, #, !, etc.)

### Componentes (Integración)
- Objetivo de prueba 
	- Verificar que un grupo de componentes interactúa (a través de interfaces) de acuerdo a las especificación técnica 
- Objeto: 
	- Conjuntos relacionados de clases, módulos, etc. 
- Entorno: 
	- Ambiente de desarrollo 
- Errores posibles: 
	- uso incorrecto de interfaz 
	- sincronización 
	- interpretación errónea

#### Técnicas de prueba
- No incremental 
	- Big-Bang 
- Incrementales (y jerárquicas) 
	- Bottom-Up (Ascendente) 
	- Top-Down (Descendente) 
- Integración Backbone (esqueleto)

### Del Sistema
- Objetivo de prueba 
	- Verificar que el sistema cumple con los requerimientos funcionales y no funcionales ● Objeto: 
	- Sistema integrado como un todo 
- Entorno: 
	- Ambiente similar al productivo ( en general ambiente de desarrollo) 
- ¿Es una prueba de componentes? 
	- Integrar los componentes desarrollados por diferentes miembros del equipo o subequipos 
	- Se centran en las interacciones
#### Técnicas de prueba
- Pruebas basadas en casos de uso 
	- Varios componentes involucrados, se fuerzan interacciones 
- Pruebas basadas en HU