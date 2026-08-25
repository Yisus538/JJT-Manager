# qa/ — JJT Manager

Dueño: **Jesus Manuel Martinez** (QA y QC).

## Alcance

Esta carpeta es del integrante de QA/QC. Contiene planes de prueba, casos de prueba, test suites (unitarias/integración/E2E), reportes de bugs, checklists de criterios de aceptación y evidencia de validación (ej. contra el ambiente de homologación de ARCA).

## Reglas para agentes de IA — acceso ampliado

A diferencia de Frontend y Backend, QA/QC tiene acceso de lectura **y escritura** tanto en `../frontend/` como en `../backend/`, además de esta carpeta, porque su rol requiere:

- Escribir tests (unitarios, de integración, E2E) dentro del código de frontend y backend.
- Corregir bugs menores detectados durante testing cuando así se acuerde con el dueño de esa carpeta.
- Leer el código de ambos módulos para diseñar casos de prueba realistas.

## Buenas prácticas igual

- Aun con acceso ampliado, evitá cambios de arquitectura o de alcance en `frontend/`/`backend/` sin coordinar con su dueño — el acceso es para testing y fixes acotados, no para rediseñar.
- Documentá bugs y resultados de testing en `qa/` (no solo como comentarios de código), para que quede trazable en la gestión del proyecto.
- Podés leer y escribir en `../docs/` libremente (ej. planes de prueba a nivel de gestión, criterios de aceptación).
