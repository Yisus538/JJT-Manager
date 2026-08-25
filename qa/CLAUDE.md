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

## Deuda técnica: quién la resuelve

QA/QC es quien más deuda técnica va a detectar (por su acceso cruzado a frontend y backend), pero **no siempre debe resolverla directamente** — por separación de funciones: si QA arregla lo mismo que QA detecta, nadie valida ese fix con ojo independiente.

- **Deuda chica y aislada** (typo, null check, función suelta sin refactor de comportamiento, mejora de legibilidad puntual): QA/QC la arregla directamente, sin pedir permiso — es más eficiente que interrumpir al dueño de esa carpeta por algo trivial.
- **Deuda grande o arquitectónica** (rediseño de un módulo, cambio de estructura de datos, cambio que afecta varios archivos o el contrato entre frontend y backend): QA/QC **la registra** (en `qa/`, con severidad e impacto) y **la asigna de vuelta** al dueño de esa carpeta — quien conoce mejor esa parte del sistema decide el cómo. Tomás Disandro (Director de Proyecto) prioriza cuándo se aborda frente al resto del backlog.
- En ambos casos, QA/QC mantiene su rol de validación: si otro integrante resuelve la deuda, QA/QC verifica el resultado de forma independiente antes de darla por cerrada.

El registro vive en `qa/TECH_DEBT.md` (ítems abiertos, por severidad) y `qa/TECH_DEBT_RESUELTO.md` (histórico de cerrados). Todo ítem nuevo, resuelto, o creado a raíz de verificar otro (patrón común: verificar un fix destapa un bug distinto) se anota ahí, con su `TD-XXX` y el changelog en el encabezado del archivo.
