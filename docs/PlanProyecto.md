JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Plan de Proyecto**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-12 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Horizonte | 27 semanas (19/08/2026 – 21/02/2027; semanas contadas desde el lunes 17/08/2026) |
| Fecha / Versión / Estado | 07/10/2026 · 1.2 · Borrador para revisión |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 05/10/2026 | Emisión inicial (borrador). |
| 1.1 | 06/10/2026 | Pasa a formato Markdown. El registro de documentos refleja las versiones vigentes (Acta v1.2 y documentos 02 a 12 en v1.1) y los archivos reales del repositorio. Se actualiza el estado de las 7 observaciones de consistencia de la v1.0 y se agregan las surgidas de la revisión del 06/10/2026 (§5). La matriz de trazabilidad usa los 7 objetivos específicos del Acta v1.2 y los criterios de éxito, e incorpora las actividades de QA. Se eliminan citas bibliográficas internas. |
| 1.2 | 07/10/2026 | Registro de documentos actualizado (Acta v1.3; Lista, Cronograma, Estimación, Riesgos, Calidad y Comunicaciones v1.2). Trazabilidad: Facturación incorpora 9.3 y H4, y los objetivos 4–7 tienen riesgos asociados. Nuevas observaciones 16 a 18 (cierre de la revisión del 07/10/2026); Alcance v1.2. |

> Plan de proyecto. Documento integrador que explica cómo se ejecutará, monitoreará y cerrará el proyecto. Organiza la documentación en las 12 secciones de un plan de proyecto, identifica qué documentos faltaban y los incorpora, y fija la trazabilidad completa objetivo → requerimiento → EDT → hito → riesgo → prueba. Responde: ¿qué?, ¿quién?, ¿cuándo?, ¿con qué?, ¿cuánto?, ¿qué puede salir mal? y ¿cómo sabremos que vamos bien?

## **1. Resumen del proyecto**

*Síntesis de los documentos vigentes.*

| Campo | Detalle | Fuente |
| :---- | :---- | :---- |
| Proyecto | Sistema de Gestión y Facturación Ágil integrado con ARCA (JJT Manager) | JJT-GPI-01 |
| Objetivo general | Sistema de gestión comercial multirubro: stock, facturación electrónica con ARCA, clientes/proveedores y cuentas corrientes, múltiples medios de pago y giftcards, reportes. | JJT-GPI-01 |
| Alcance | 7 módulos incluidos (RF-01 a RF-32) y 6 exclusiones explícitas (RNF-07, RF-21). | JJT-GPI-03, 04 |
| Plazo | 27 semanas: 19/08/2026 – 21/02/2027; hitos H1 (sem. 6), H2 (sem. 15), H3 (sem. 23), H4 (sem. 27). | JJT-GPI-01, 07 |
| Esfuerzo y costo | 970 h esperadas (rango 760–1.220 h); presupuesto techo de 1.080 h = USD 27.000 de personal (970 h de línea base + 110 h de reserva) + USD 25 de infraestructura = USD 27.025. | JJT-GPI-08 |
| Equipo | Tomás Disandro (Director y Backend), Juan Cruz Bulatovich (Frontend), Jesus Manuel Martinez (QA/QC); Sponsor: Julio Gutierrez. | JJT-GPI-01 |
| Metodología | Híbrida: fases predictivas para planificación (H1) y cierre (H4); desarrollo iterativo en sprints de 2 semanas entre ambas (S1–S8). | JJT-GPI-01, 04, 07 |
| Riesgos principales | R1 (WS de ARCA) y R2 (scope creep), nivel 12; exposición total esperada USD 3.680 (147 h) frente a una reserva de USD 2.750 (110 h). | JJT-GPI-09 |

## **2. Estructura del plan y análisis de brechas**

| N.º | Sección del plan | Documento(s) que la cubren | Estado |
| :----: | :---- | :---- | :---- |
| 1 | Resumen y objetivos | JJT-GPI-01 Acta de Constitución (y §1 de este documento) | Cubierta |
| 2 | Alcance y entregables | JJT-GPI-04 Alcance y Gestión; JJT-GPI-03 Requerimientos | Cubierta |
| 3 | EDT / WBS | JJT-GPI-05 EDT; JJT-GPI-06 Lista de Actividades | Cubierta |
| 4 | Cronograma e hitos | JJT-GPI-07 Cronograma (hitos también en JJT-GPI-04 §3) | Faltaba — nuevo |
| 5 | Recursos y organización | JJT-GPI-04 §4 (equipo) y JJT-GPI-08 §4–5 (esfuerzo por rol, capacidad) | Parcial — completado |
| 6 | Costos y presupuesto | JJT-GPI-08 Estimación y Presupuesto (presupuesto de alto nivel en JJT-GPI-01) | Faltaba — nuevo |
| 7 | Calidad y pruebas | JJT-GPI-10 Plan de Calidad y Pruebas | Faltaba — nuevo |
| 8 | Riesgos | JJT-GPI-09 Plan de Gestión de Riesgos (2 riesgos de alto nivel en JJT-GPI-01 y 04) | Faltaba — nuevo |
| 9 | Comunicaciones | JJT-GPI-11 Plan de Comunicaciones y Seguimiento | Faltaba — nuevo |
| 10 | Gestión de cambios | JJT-GPI-04 §7 (control de cambios); JJT-GPI-10 §8 (configuración y versiones) | Cubierta / completada |
| 11 | Supuestos y restricciones | JJT-GPI-01, 03 y 04 (supuestos y restricciones consistentes entre sí) | Cubierta |
| 12 | Criterios de aceptación | JJT-GPI-01 y 04 (criterios de éxito) y JJT-GPI-10 §1 (CE-1 a CE-3 con verificación) | Cubierta / completada |

Además de las 12 secciones, el seguimiento y control del plan estaba sin documentar: queda cubierto en JJT-GPI-11 (§3 a §8).

## **3. Registro de documentos**

*12 documentos · todos en formato Markdown en `docs/`.*

| Código | Documento | Fecha | Versión | Estado | Ubicación |
| :---- | :---- | :---- | :----: | :---- | :---- |
| JJT-GPI-01 | Acta de Constitución del Proyecto | 19/08/2026 (rev. 07/10/2026) | 1.3 | Vigente · aprobación del sponsor pendiente | `docs/Acta Constitucion.md` |
| JJT-GPI-02 | Registro de Interesados | 25/08/2026 (rev. 06/10/2026) | 1.1 | Vigente | `docs/StakeHolders.md` |
| JJT-GPI-03 | Documento de Requerimientos | 25/08/2026 (rev. 06/10/2026) | 1.1 | Vigente | `docs/Requerimientos.md` |
| JJT-GPI-04 | Documento de Alcance y Gestión | 25/08/2026 (rev. 07/10/2026) | 1.2 | Vigente | `docs/Alcance.md` |
| JJT-GPI-05 | Estructura de Desglose del Trabajo (EDT) | 26/08/2026 (rev. 06/10/2026) | 1.1 | Vigente | `docs/EDT.md` |
| JJT-GPI-06 | Lista de Actividades | 26/08/2026 (rev. 07/10/2026) | 1.2 | Vigente | `docs/ListaActividades.md` (PDF: `docs/ListaActividades-JJT-Manager.pdf`) |
| JJT-GPI-07 | Cronograma del Proyecto | 07/10/2026 | 1.2 | Borrador para revisión | `docs/Cronograma.md` (Gantt en PDF: `docs/Cronograma_Gantt_JJT_Manager.pdf`) |
| JJT-GPI-08 | Estimación de Esfuerzo y Presupuesto | 07/10/2026 | 1.2 | Borrador para revisión | `docs/EstimacionPresupuesto.md` |
| JJT-GPI-09 | Plan de Gestión de Riesgos | 07/10/2026 | 1.2 | Borrador para revisión | `docs/PlanRiesgos.md` |
| JJT-GPI-10 | Plan de Calidad y Pruebas | 07/10/2026 | 1.2 | Borrador para revisión | `docs/PlanCalidad.md` |
| JJT-GPI-11 | Plan de Comunicaciones y Seguimiento | 07/10/2026 | 1.2 | Borrador para revisión | `docs/PlanComunicaciones.md` |
| JJT-GPI-12 | Plan de Proyecto (documento integrador) | 07/10/2026 | 1.2 | Borrador para revisión | `docs/PlanProyecto.md` |

*Los códigos JJT-GPI-NN son una convención propuesta en este plan para identificar y citar cada documento; cada documento lo declara en su encabezado. Los borradores v1.0 de los documentos 07 a 12 (PDF, 05/10/2026) quedan en `docs/extras/DOCS Faltantes/` solo como referencia histórica: están reemplazados por las versiones Markdown indicadas.*

## **4. Matriz de trazabilidad integral**

*Objetivo → RF → EDT → hito → riesgo → prueba.*

| Objetivo / elemento del Acta v1.2 | Requerimientos | EDT | Hito | Riesgos | Pruebas |
| :---- | :---- | :---- | :----: | :---- | :---- |
| Obj. 1 — Modelo de datos genérico multirubro | RNF-01 a 03, RF-32 | 2.2, 2.4, 9.2 | H1, H4 | R8 | PC-GEN |
| Obj. 2 — Facturación electrónica integrada con ARCA | RF-06 a 11, RNF-04, 05, 09 | 2.3, 4.0, 9.3 | H1, H2, H4 | R1, R3, R4, R7, R9, R12 | PC-ARCA, PC-HOM |
| Obj. 3 — Control de stock | RF-01 a 05 | 3.0 | H2 | R6 | PC-STK |
| Obj. 4 — Clientes, proveedores y cuentas corrientes | RF-12 a 14 | 5.0 | H3 | R6, R10 | PC-CLI |
| Obj. 5 — Medios de pago y giftcards | RF-15 a 21 | 6.0 | H3 | R6, R10 | PC-PAG |
| Obj. 6 — Reportes y estadísticas exportables | RF-22 a 27 | 7.0 | H3 | R6, R11 | PC-REP |
| Obj. 7 — Usuarios y permisos | RF-28 a 30 | 8.0 | H3 | R2, R11 | PC-USR |
| Criterio de éxito 2 — Ciclo integral del sistema | RF-31 | 9.1 | H4 | R11 | PC-E2E |
| Restricciones y alcance (equipo fijo, control de cambios, interfaz web, exclusiones) | RNF-06 a 08, 10 | 1.0, 9.4 | H1, H4 | R2, R5, R10 | PC-NF |

*Los riesgos transversales a todos los módulos (R2, R5, R6, R10, R11) afectan a cada fila; se listan solo donde son el riesgo principal. Las actividades de QA de cada módulo (1.5, 2.4, 3.5, 4.7, 5.4, 6.5, 7.7, 8.3) ejecutan las pruebas de la columna final (Plan de Calidad §5). Lectura: un objetivo del Acta se traza hacia adelante a sus requerimientos, a los paquetes de la EDT que lo construyen, al hito en que se entrega, a los riesgos que lo amenazan (JJT-GPI-09) y a las pruebas que lo verifican (JJT-GPI-10). Las referencias a requerimientos y a la EDT se verificaron contra JJT-GPI-03 y JJT-GPI-05 v1.1.*

## **5. Observaciones de consistencia**

*Hallazgos al cruzar los documentos. Estado al 06/10/2026.*

| N.º | Observación | Documento / ubicación | Estado | Resolución / acción |
| :----: | :---- | :---- | :---- | :---- |
| 1 | RF-28 (al menos dos roles) no figuraba en la EDT. | JJT-GPI-05 §8.0; JJT-GPI-04 §1 | Resuelta | RF-28 agregado a 8.1 y 8.2 en EDT v1.1 y Alcance v1.1. |
| 2 | Numeración de encabezados de la EDT en la extracción del Documento de Alcance. | JJT-GPI-04 §2 | Resuelta | Los documentos están en Markdown con numeración explícita; el Alcance remite a EDT.md como versión de referencia. |
| 3 | Grafía del nombre del integrante de QA («Martines»). | JJT-GPI-01 | Resuelta | Unificado en Acta v1.1; además se unifica «Tomás» y «Jesus» en todos los documentos. |
| 4 | QA descrito como transversal, pero programado solo en el paquete 9.0 (240 h sin actividad). | JJT-GPI-04 §4; JJT-GPI-06; JJT-GPI-08 §4 | Resuelta | 8 actividades de QA por módulo en Lista v1.1 (1.5, 2.4, 3.5, 4.7, 5.4, 6.5, 7.7, 8.3), con las 240 h de Jesus. |
| 5 | El Acta listaba los reportes sin rentabilidad. | JJT-GPI-01 | Resuelta | Alineado en Acta v1.1. |
| 6 | Carga semanal por encima de 40 h (pico de 83 h) y H2 al 101%. | JJT-GPI-07 §6; JJT-GPI-08 §5 | Mitigada | Calendario nivelado en Cronograma v1.1: pico de 47,8 h y 10 semanas entre 40 y 50 h. La demanda de H2 (365 h) sigue superando en 5 h su capacidad: se cubre con la reserva (decisión del Sponsor si se consume). |
| 7 | El presupuesto de USD 27.000 del Acta cubría solo personal. | JJT-GPI-01; JJT-GPI-08 §6 | Resuelta | Acta v1.1 declara ambos rubros (USD 27.025). |
| 8 | **Nueva.** Los documentos se citan como «aprobados» pero ninguna aprobación está firmada (Acta, secciones de aprobación vacías; v1.1/v1.2 modifica fecha y presupuesto). | JJT-GPI-01 §12; JJT-GPI-07; JJT-GPI-10 | Abierta | Redacción corregida (se dice «vigente»/«pendiente de aprobación»). Falta la firma del Sponsor y del equipo. |
| 9 | **Nueva.** La compuerta H1 (semana 6, 27/09/2026) ya venció y no hay en `docs/` evidencia de 1.5, 2.1, 2.2, 2.3 y 2.4 ni acta de revisión de hito. | JJT-GPI-07 §7; JJT-GPI-10 §7 | Abierta | Confirmar el estado real de 2.1–2.3 y documentarlo (o replanificar por control de cambios); realizar la revisión de H1. |
| 10 | **Nueva.** La exposición esperada de riesgos (147,2 h) supera la reserva (110 h) por 37,2 h, y la reserva coincide con la holgura de capacidad. | JJT-GPI-09 §4; JJT-GPI-08 §5 | Gestionada | Reserva asignada por prioridad (R1, R2, R5, R11, R10, R6); R7, R8, R3, R4 y R9 sin reserva, con escalamiento al Sponsor si se materializan. |
| 11 | **Nueva.** Dependencias lógicas invertidas en 6.0 (QR antes de la pasarela; cuenta corriente antes de 5.2) y precedencia 3.4 → 5.1 sin justificación. | JJT-GPI-06 | Resuelta | Lista v1.1: 6.4 antecede a 6.1.3, 6.1.1 sigue a 5.2, se elimina 3.4 → 5.1. |
| 12 | **Nueva.** El Documento de Alcance §5 listaba solo R1 y R2, mientras el Plan de Riesgos agrega R3 a R12. | JJT-GPI-04 §5; JJT-GPI-09 | Resuelta | Alcance v1.1 incorpora R6, R10 y R11 y remite al Plan de Riesgos para el registro completo (R1 a R12). |
| 13 | **Nueva.** Los documentos 02 a 06 no tenían código, versión ni historial de cambios, aunque el Alcance §7.4 exige incrementar la versión ante cambios. | JJT-GPI-02 a 06 | Resuelta | Todos los documentos declaran código, versión y tabla de cambios. |
| 14 | **Nueva.** Redacción no apta para el sponsor: un supuesto del Acta sobre quién evalúa el proceso, el riesgo R10 y citas bibliográficas internas en los documentos 08 a 12. | JJT-GPI-01, 08 a 12 | Resuelta | Reformulados en los documentos vigentes (R10 pasa a «dedicación parcial del equipo»). |
| 15 | **Nueva.** Hay dos EDT (Alcance §2 y EDT.md) con distinto nivel de detalle. | JJT-GPI-04; JJT-GPI-05 | Resuelta | El Alcance resume los paquetes y remite a EDT.md, con las mismas referencias RF/RNF. |
| 16 | **Nueva.** El esfuerzo por rol de Estimación §4 (323/324/323 h) contradecía las horas por actividad de §3: por responsable de actividad, Jesus carga 370 h (> 360 h) y Juan 265 h. | JJT-GPI-08 §3–4 | Resuelta | Estimación v1.2 §4: 63 h de apoyo entre integrantes según su rol (interfaz de 4.5, 5.1 y 5.3, y parte de 9.1, 9.2 y 9.4 para Juan; 9.3 con apoyo de Tomás). Carga final 323/324/323 h. Lista v1.2 y Alcance v1.2 lo reflejan. |
| 17 | **Nueva.** La gestión continua (reuniones, informes, registro de horas, SPI/CPI, revisiones de sprint) y los documentos 07–12 no tienen horas; las 60 h de 1.0 se consumen en 1.1–1.5. | JJT-GPI-08 §7; JJT-GPI-06 | Abierta | Declarado en Estimación v1.2. Falta decidir cómo financiarlo (actividad nueva con re-estimación o reserva). |
| 18 | **Nueva.** 4.6 (credenciales de producción) bloqueaba 5.1 y 6.1.2 pese a ser opcional según el Acta; los reportes y los roles estaban encadenados en serie; el CPM colapsaba cadenas de actividades de 1 semana. | JJT-GPI-06; JJT-GPI-07 §5–6 | Resuelta | Lista v1.2 y Cronograma v1.2: nuevas precedencias, convención de CPM y duración lógica de 26 semanas. |

## **6. Aprobación**

*Pendiente.*

| Rol | Nombre | Firma / Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Sponsor | Julio Gutierrez | | |
| Director de Proyecto | Tomás Disandro | | |
| Integrante | Juan Cruz Bulatovich | | |
| Integrante | Jesus Manuel Martinez | | |
