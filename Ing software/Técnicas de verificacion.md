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
- Habilidades y conocimiento del verificador ● Test exploratorio (si no existe documentación) ○ Descubro y conozco el software ○ Genero casos de prueba ○ Ejecutar casos de prueba