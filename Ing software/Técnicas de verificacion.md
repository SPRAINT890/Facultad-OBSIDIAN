## Revisiones
- Grupo de personas aplica capacidades analíticas para verificar y evaluar cuestiones complejas. 
- Lectura intensiva, comprensión de documentos 
- Comprobar semántica de los documentos 
- Tipos 
	- Relativas a productos (o productos intermedios, incrementos) (el programa)
	- Relativas al proyecto o proceso (El proceso de desarrollo)
- ¿Cuándo se deberían hacer las revisiones?

==Se revisan documentos como los requisitos y el diseño de arquitectura==
### Beneficios
- Mejora costos (antes se encuentre un error, es menos costoso corregirlo) 
- Minimiza fase de desarrollo, fase de pruebas dinámicas 
- Conocimiento compartido (responsabilidad compartida) 
- Si la técnica se utiliza sistemáticamente y se ejecutan de manera eficiente, se pueden detectar y reparar más del 70% de los defectos de un documento antes de que se transmitan a siguientes fases




## Tecnicas dinamicas
### Caja negra
- El objeto de prueba se considera una caja negra
- Se basan en los requerimientos o especificacion
- No considera la estructura o diseño
- Se puede usar en diferentes etapas de prueba y niveles de granularidad
- Ejemplo
	- Particiones de equivalencias
	- Pruebas basadas en requerimientos

### Caja Blanca
- El objeto de prueba es "transparente"
- Se basan en la estructura del codigo o diseño
- A nivel del codigo
	- Se busca cubrir cada parte del codigo al menos una vez
	- Sentencias, decisiones, caminos, etc
- A nivel de diseño
	- Se busca cubrir cada interacción (interfaz) al menos una vez

### Caja Gris
- Combina verificación de la funcionalidad (caja negra) con verificación parcial de la estructura (caja blanca), es decir, se empieza por una caja negra hasta encontrar un error, y luego se revisa el codigo pasando por caja blanca

### Basada en la experiencia
- No es un enfoque sistemático 
- Habilidades y conocimiento del verificador 
- Test exploratorio (si no existe documentación) 
	- Descubro y conozco el software 
	- Genero casos de prueba 
	- Ejecutar casos de prueba

## Aspectos positivos

| Estaticas                                                           | Dinamicas                                                 |
| ------------------------------------------------------------------- | --------------------------------------------------------- |
| Detección temprana de errores                                       | Comportamiento real del software                          |
| Análisis exhaustivo (herramientas)                                  | Permite validar software                                  |
| Mejora de la calidad                                                | Identifican errores relacionados con la lógica de negocio |
| Pueden aplicarse en cualquier fase del ciclo de vida del desarrollo | Detectar problemas de integración en ejecución            |

## Aspecto Negativo

| Estaticas                                                       | Dinamicas                                            |
| --------------------------------------------------------------- | ---------------------------------------------------- |
| No se ven problemas relacionados con el comportamiento dinámico | Dependencia de la cobertura de pruebas               |
| Falsos positivos (herramientas)                                 | Necesito el producto o incremento                    |
| Dependencia de herramientas                                     | Costoso en tiempo y recursos (ambiente, pruebas,etc) |

## Ambientes
### Desarrollo
- OBJETIVO: 
	- Entorno en el que los desarrolladores escriben y prueban el código. 
- CARACTERISTICAS: 
	- En general configurado en las computadoras locales de los desarrolladores o en servidores dedicados. 
	- Se utilizan herramientas de depuración (debugg)

### Integración Continua (CI - Continuous Integration)
 - OBJETIVO: 
	 - Automatiza el proceso de prueba y construcción del software cuando se integra 
 - CARACTERISTICAS: 
	 - Cada vez que se introduce un cambio en el código, el sistema de CI ejecuta automáticamente una serie de pruebas 
	 - Se detectan errores a nivel de integración, lo que facilita el trabajo en equipo.
### Pruebas (Testing o QA - Quality Assurance)
-  OBJETIVO: 
	- Probar el software en condiciones controladas 
- CARACTERISTICAS: 
	- Similar al ambiente de producción en términos de configuración y funcionalidades. 
	- Se ejecutan pruebas automatizadas y manuales sobre versiones de software 
	- Se utilizan para pruebas funcionales, de rendimiento, de seguridad, etc..

### Staging o Preproducción
- OBJETIVO: 
	- Entorno “espejo" del ambiente de producción. 
- CARACTERISTICAS: 
	- Casi idéntico al ambiente de producción en cuanto a configuración, datos, etc 
	- Se usa para realizar las últimas pruebas 
	- Se puede simular cómo se comportará el sistema en producción, asegurando que todos los problemas hayan sido resueltos.
### Producción (Production)
- OBJETIVO: 
	- Entorno en el que los usuarios finales interactúan con el sistema. 
- CARACTERISTICAS: 
	- Accesible a los usuarios finales. 
	- Entorno real donde el software está en uso por los clientes o usuarios. 
	- Se emplean herramientas de monitoreo para asegurar que el sistema esté funcionando correctamente.