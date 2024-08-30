- Dentro o fuera
- Comparacion por pares y ranking
- $100, se te da 100 dolares y tenes que distribuir la plata
- Escala de 3 niveles
	![[Pasted image 20240830182451.png | 500]]
- MoSCoW
	- Must: El requisito debe satisfacerse para que la solucion se considere un exito
	- Should: El requisito es importante y debe incluirse en la solución si es posible, pero no es obligatorio para el éxito. 
	- Could: Es una capacidad deseable, pero que podría diferirse o eliminarse. Implementarla solo si el tiempo y los recursos lo permiten. 
	- Won’t: Esto indica un requisito que no se implementará en este momento, pero podría incluirse en una versión futura. 

## Validación de requisitos
- Proceso por el cual se determina si los requisitos relevados son consistentes con las necesidades del cliente.
- Busca encontrar problemas en los requisitos

¿Por que necesito validar los requisitos?
Para saber efectivamente que los requisitos son los que quiere el cliente
No se tiene capacidad, tiempo o presupuesto

- Es difícil definir todos los requisitos 
- Cuando se ve el software funcional 
	- Surgen nuevos requisitos 
	- Se encuentran bugs o errores 
	- Requisitos se vuelven obsoletos 
- El entorno empresarial y técnico cambian 
- Cliente vs Usuario final 
	- Muchas veces el cliente no es el usuario final, por ende puede que el cliente no tenga el conocimiento con el usuario final
- Muchos interesados

### Fases de validación
- Chequear validez 
	- ¿Se reflejan las necesidades reales de los usuarios del sistema? 
- Verificar coherencia 
	- ¿Hay requisitos en conflicto?
- Comprobar integridad
	- ¿Están todas las funciones requeridas por el cliente? 
- Verificar realismo 
	- ¿Los requisitos se pueden implementar con el presupuesto y tecnología disponibles? 
- Verificabilidad 
	- ¿Puedo escribir un conjunto de pruebas que me permita verificar los requerimientos?


### ¿Por qué surgen las metodologías ágiles? 
- Mercado competitivo 
	- Responder a nuevas necesidades de negocio 
	- Adaptarse rápidamente a nuevas oportunidades del mercado 
- No se pueden derivar requerimientos estables 
	- Los requisitos pueden ser más claros cuando los usuarios interactúan con el software
- Cambio de paradigma 
	- Desarrollo y entrega rápido vs. calidad 
- Contexto cambiante 
	- Tecnológico, necesidades
- Desarrollo incremental 
	- Incrementos “pequeños” 
	- Se crean nuevas versiones del sistema 
	- Se liberan al cliente al finalizar un período o sprint 
- Se involucra al cliente en el proceso 
	- Acelerar el feedback 
- Minimiza documentación 
	- Prioriza comunicación informal antes comunicación formal y documentos estrictos 
- Diseño e implementación 
	- Obtención de requisitos y validación se entrelazan con estas etapas 
- Herramientas de soporte 
	- Automatizar verificaciones, liberación, configuraciones, etc

### Manifiesto Ágil
- **Individuos e interacciones** sobre procesos y herramientas. 
	-  Todas las personas tienen que autogestionarse
- **Software funcional** sobre documentación completa. 
- **Colaboración del cliente** sobre la negociación contractual. 
- **Responder al cambio** sobre el seguir un plan.


## Extreme Programing (XP)
### Historia de usuario
“Descripción breve y simple de una característica contada desde la perspectiva de la persona (usuario, cliente o interesado) que desea una nueva funcionalidad o capacidad”

### Programación en pares
- Los desarrolladores trabajan juntos para programar 
- Los pares cambian 
- Fomenta la propiedad y responsabilidad colectiva 
- Proceso de revisión informal 
- Fomenta la refactorización

### Desarrollo dirigido por pruebas
- Enfoque para abordar pruebas (verificación) sin especificación 
- Se diseñan y desarrollan las pruebas antes de implementar 
- Desarrollo de pruebas incremental basado en HU 
- El cliente participa en el desarrollo y validación de la prueba 
- Basado en la automatización 
- Puedo ejecutar la prueba durante el desarrollo, para descubrir los problemas antes