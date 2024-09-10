- Entender y definir cómo debe diseñarse la estructura global de un sistema 
- Es la primera fase del proceso de diseño de software 
- En procesos ágiles, se define en los primeros sprints (en general) 
- Estructuras de componentes de software, cómo se relacionan y las propiedades externas que tienen
- Proceso creativo que depende de 
	- Sistema a crear 
	- Antecedentes 
	- Experiencia de los arquitectos 
- Los requerimientos no funcionales determinan parte de la arquitectura
- Representación que permite 
	- Cumplir con los requerimientos 
	- Identificar alternativas arquitectónicas cuando aún es posible 
	- Reducir los riesgos en la construcción de software

## Nivel de Abstraccion
- La arquitectura en pequeño (detallada) 
	- Arquitectura de programa particular 
	- Se centra solo en los componente de ese programa particular 
- La arquitectura en grande (alto nivel) 
	- Arquitectura de sistemas empresariales complejos 
	- Varios sistemas, programs, componentes 
	- Sistemas distribuídos

## Ventajas: Definir y documentar
- Comunicación 
	- Dado que es una descripción a alto nivel puede ser una herramienta de discusión e intercambio con múltiples interesados 
- Análisis del sistema 
	- Impacto directo sobre los requerimientos no funcionales 
	- Plasma requerimientos funcionales 
- Reutilización a gran escala 
	- La arquitectura del sistema es la misma para sistemas con requerimientos similares 
	- Reutilización de software a gran escala

## Guía para decisiones creativas
- ¿Existe una arquitectura de aplicación genérica que pueda usar como template? (patrones de diseño) 
- ¿Cómo se distribuye el sistema? 
- ¿Cómo puedo agrupar los componente del sistema? 
- ¿Quién valida la arquitectura? 
- ¿Cuál es el mejor diseño arquitectónico para cumplir los RNF? 
- ¿Se requiere documentación? (Que nivel de documentacion se requiere)
- Los sistemas en el mismo dominio de aplicación tienen arquitecturas similares (en general). Ejemplo: salud, fintech, educación 
- Pueden basarse en patrones, estilos de arquitectura genéricos (independientes del dominio)

## Requerimientos No Funcionales
### Rendimiento
- Identificar funciones críticas 
- Agruparlas para evitar incremento de comunicaciones 
- Escalar el sistema
### Seguridad
- Arquitectura en capas 
- Proteger activos críticos 
- Agrupar funciones de seguridad

### Disponibilidad
- Componentes redundantes 
- Sistemas tolerantes a fallas

### Mantenibilidad
- Componentes fáciles de modificar 
- Evitar estructuras de datos compartidas

## Escalado Horizontal
Replico la instancia

## Escalado Vertical
Aumento los recursos del modulo

## Vista 4+1

### Logica
- Abstracciones como objetos o clases de objetos 
- Relaciona requerimientos del sistema con entidades

### Procesos
- Interacción en tiempo de ejecución (usuarios->funcionalida des)

### Desarrollo
- Cómo se compone el software en elementos de desarrollo

### Fisica
-Hardware del sistema y cómo se distribuye


