# ADR [0001]: Ataque por Inyección SQL

## Context

La inyección SQL es un tipo de ataque donde una persona puede ejecutar comandos SQL no autorizados en una base de datos. 
Esto puede provocar en acceso no autorizado a datos sensibles, modificación de datos, o eliminación de información.
Según OSAP este tipo de ataque está en tercer lugar del top 10 de ataques donde el 94% de las aplicaciones que se probaron para alguna forma de inyección, con una tasa de incidencia máxima del 19%, una tasa de incidencia promedio del 3% y 274.000 ocurrencias. 
Esto demuestra que es primordial poder prevenir este tipo de ataques en nuestros sistemas.

## Decision

Implementar medidas para prevenir inyecciones SQL en las aplicaciones MuleSoft mediante el uso de consultas parametrizadas y validación de entradas.
Aplicar validación de esquemas utilizando el enrutador de APIkit o esquemas XML/JSON. 
Proteger la API agregando tipos de datos y valores en la definición RAML.
Realizar pruebas exhaustivas para asegurar que las modificaciones no introduzcan nuevos errores y que las medidas de seguridad funcionen como se espera.
Implementar monitoreo continuo para detectar intentos de inyección SQL.

## Status

Aceptado.

## Consequences

Beneficios:
- Mejora de Seguridad: Reducción significativa del riesgo de inyección SQL.
- Cumplimiento Normativo: Cumplimiento con normas y regulaciones de seguridad de datos.
- Confianza del Cliente: Aumento de la confianza de los clientes en la seguridad del sistema.

Inconvenientes:
- Complejidad Adicional: Aumenta la complejidad del desarrollo y mantenimiento del código.
- Requiere Capacitación: Los desarrolladores necesitan estar capacitados en el uso de consultas parametrizadas y técnicas de validación/sanitización.

## Related documents

- https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html
- https://docs.mulesoft.com/mule-sdk/latest/security-best-practices

### References
- https://owasp.org/Top10/A03_2021-Injection/
- https://help.mulesoft.com/s/question/0D52T00004mXXTOSA4/best-practices-to-prevent-sql-injections
- https://www.ingenierobinario.com/mulesoftarchitect101/
