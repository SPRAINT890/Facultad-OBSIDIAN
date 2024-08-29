[[Clei/Curso 5/Practico 1]]
[[DF vs IR]]
[[Clei/Curso 5/Laboratorio 1]]
[[Tipo de Malware y Ataques]]
## Historia

1976, Libro Crime by computer (Donn Parker)
1984, Se funda el CART (Computer Analysis and Response Team) fue creado para proveer soporte a agentes del FBI
1993, Primera conferencia internacional sobre evidencia en computadoras
1995, se funda  el IOCE
2000, 

### CART
"Para abordar de manera razonable la necesidad legitima de las fuerzas del orden de acceder a dispositivos y a la información que contienen con un enfoque estructurada para examinar las pruebas y preservadas para poder llevar a tribunales"

### Organismo encargados de hacer cumplir la ley
Utilizan pruebas digitales para ayudar a condenar a absolver a los sospechosos
### Equipos de respuestas a incidentes informáticos
Estos equipos son los primeros en responder a los ataques cibernéticos

### Objetivo
Realizar una investigación en pautas, y plasmarlo en un informe para poder utilizarlo en tribunales

## Interpretación
### Interpretación  1
disciplina de las ciencias forenses que, considerando las tareas propias asociadas con la evidencia, procura descubrir e interpretar la información en los medios informáticos para establecer los hechos y formular las hipótesis relacionadas con el caso

### Interpretación 2
disciplina científica y especializada

### Definición de CiberCrimen
- Crimen dirigido contra una computadora
- Crimen del que una computadora contiene evidencia
- Crimen donde la computadora es usada como una herramienta para realizar el mismo

Un equipo informático puede ser un instrumento, la evidencia de un delito o la combinación de los aspectos

Al principio, la mayoría de la evidencia digital se encontraba en sistemas informáticos y dispositivos de TI (Informática Forense)
- Computadoras personales, servidores, teléfonos móviles, etc


RFC3227, la evidencia necesita ser:
- Admisible
- Autentica
- Completa
- Fiable
- Creíble


### Tipos de evidencia
#### Datos volátiles
Los datos volátiles refieren a los datos temporales en un dispositivo digital que necesitan un suministro de energía continuo y se eliminan si se interrumpe el suministro de energía. Ejemplos: Usuarios logueados, archivos abiertos, información de red, información de procesos, mapeo procesos puertos, memoria de procesos.

#### Datos no volátiles
Los datos no volátiles se refieren a los datos permanentes que se guardan en dispositivos de almacenamiento secundarios, como discos duros. No dependen del suministro de energía y permanecen intactos al apagar. Ejemplos: Archivos ocultos, espacio slack, archivo swap, particiones no usadas, log de eventos


#### Metadatos
información subyacente que no es perceptible por el usuario final
#### Datos replicantes
datos que se duplican para protegerse contra la perdida de datos
#### Datos residuales
datos que se pueden haber eliminados, pero aun siguen presentes

### Principios a tener en cuenta
- Principio de intercambio de locard:
  "Cuando dos objetos entran en contacto, dejan un rastro el uno con el otro"
  
- Indeterminación o de incertidumbre de Heisenberg
  "No es posible estudiar algo sin que ello conlleve alteración alguna"
  
- El principio de economía o la "Navaja de Ockham"
  "Cuando nos encontramos frente a dos teorías o hipótesis que en igualdad de condiciones producen las mismas consecuencias, entonces, aquella hipótesis o teoria mas simple posee mas probabilidades de ser la correcta"

### Requisitos durante el manejo
- Auditable: Los procesos realizados deberían estar disponibles para una evaluación independiente a fin de determinar si se siguió un método, una técnica o procedimiento científico apropiado
- Repetible: Un actor debidamente capacitado y experimentado debe ser capaz de llevar a cabo todos los procesos descritos en la documentación y llegar a una conclusión
- Reproducible: Se puede obtener los mismos resultados independientemente de la herramienta
- Justificable: El investigador actuante debe ser capaz de justificar todas las acciones llevadas a cabo en cuanto al manejo de la información

## Proceso forense digital

### Identificación
es la búsqueda y el reconocimiento, documentación de la potencial evidencia digital, a su vez se deben identificar los medios de almacenamiento los dispositivos de procesamiento que pueden contener evidencia y sea relevante para el caso

"actor first responder" de cuando se encuentra un dispositivo sospechoso encontrado

- Identificar el registro de conectividad ISP
- servidores de correos electrónicos externos

### Preservación
- una vez identificada la evidencia, es importante protegerla de cualquier tipo de modificación o eliminación
- El proceso de preservación implica la salvaguarda de las posibles pruebas digitales y de los dispositivos digitales que puedan contenerlas contra la manipulación o la destrucción de los mismos
- Es un proceso que 

Durante un proceso de investigación de un dispositivo, hay una buena practica la cual es que este presente un escribano o abogado para que pueda certificar, todas las acciones que hacemos a la evidencia.

### Recopilación
Una vez identificados los dispositivos, se debe decidir que paso seguir, recopilar o adquirir, es un proceso en donde los dispositivos que pueden contener evidencias se envían un ambiente controlado (laboratorio) para su manejo

### Adquisición
no es una interpretación de los datos, solo es el acto de copiar datos a un dispositivo separado

## Análisis
En la fase de análisis se debe interpretar la información extraída, se deben analizar y estudiar los datos relevantes, se debe identificar datos escenciales y los no escenciales.