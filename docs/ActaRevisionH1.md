JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Acta de Revisión de Hito H1**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-18 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Elaboró | Jesus Manuel Martinez (QA y QC) |
| Hito revisado | H1 — Planificación, arquitectura y diseño (fecha objetivo 27/09/2026) |
| Fecha / Versión / Estado | 03/11/2026 · 1.0 · Borrador: pendiente de conformidad del Director |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 03/11/2026 | Evaluación de la compuerta H1 contra el Plan de Calidad §7 y el Cronograma §7. Resultado: no aprobada; falta el spike 2.3. |

> Cierra la observación 9 del Plan de Proyecto en lo que respecta al registro de la revisión. El resultado negativo se documenta tal cual; el hito no puede darse por aprobado hasta cumplir la condición pendiente.

## **1. Evaluación de la compuerta**

*Criterios de salida de H1: Plan de Calidad (JJT-GPI-10) §7.*

| Criterio | Evidencia | Resultado |
| :---- | :---- | :---- |
| Documentos de gestión aprobados | Aprobación del Sponsor confirmada el 07/10/2026 (Plan de Proyecto, obs. 8) | Cumplido (con 6 semanas de retraso en el registro) |
| Revisión de pares 1.5 cerrada | JJT-GPI-13 | Cumplido (ejecutada en la sem. 8, prevista en 2–5) |
| Stack tecnológico definido (2.1) | JJT-GPI-14 | Cumplido |
| Modelo de datos genérico definido (2.2) | JJT-GPI-15 | Cumplido |
| Modelo revisado contra dos rubros (2.4) | JJT-GPI-16 (doce escenarios resueltos por datos) | Cumplido |
| Spike con conexión a homologación documentada y un CAE de homologación obtenido (2.3) | No hay documento de spike ni evidencia de CAE en el repositorio | **No cumplido** |
| Criterios CE-1 a CE-3 acordados | Definidos en Plan de Calidad §1 y aprobados con la documentación | Cumplido |

## **2. Decisión**

**H1: NO APROBADO.** Cumple 6 de 7 criterios. El criterio pendiente es el de mayor riesgo: es el que des-riesga la ruta crítica (R1).

H2 está en ejecución sin cumplir la salida de H1. Esta acta lo declara como **desvío**: el equipo continúa con las tareas que no dependen del spike, y las que sí dependen (3.1, 4.1.1 a 4.7) quedan condicionadas a su cierre.

## **3. Condiciones para cerrar H1**

| N.º | Condición | Responsable | Fecha límite |
| :---- | :---- | :---- | :---- |
| 1 | Ejecutar el spike 2.3 con la CUIT de prueba (R4 confirmado): conexión a WSAA/WSFEv1 en homologación y CAE de una factura de prueba | Tomás | 10/11/2026 |
| 2 | Documentar el resultado del spike en `docs/` (procedimiento, dificultades, evidencia del CAE sin credenciales ni CUIT reales, RNF-04) | Tomás | 12/11/2026 |
| 3 | Verificar el documento y la ausencia de secretos en el repositorio | Jesus | 13/11/2026 |
| 4 | Emitir la versión 2.0 de esta acta con la aprobación del hito | Jesus y Tomás | 13/11/2026 |

Si la condición 1 no se cumple en la fecha límite, se aplica la contingencia de R1 (Plan de Riesgos): librería de terceros probada y replanificación de H2 por control de cambios (Alcance §7).

## **4. Aprobación**

| Rol | Nombre | Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Elaboró (QA/QC) | Jesus Manuel Martinez | | |
| Director de proyecto | Tomás Disandro | | |
| Sponsor | Julio Gutierrez | | |
