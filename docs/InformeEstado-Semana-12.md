JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Informe de Estado — Semana 12**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-17 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Elaboró | Jesus Manuel Martinez (QA y QC) |
| Período | Semanas 9 a 12 (hasta el 03/11/2026; último informe: semana 8, 07/10/2026) |
| Fecha / Versión / Estado | 03/11/2026 · 1.0 · Borrador para validar con Tomás y Juan |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 03/11/2026 | Emisión inicial. Estado construido solo con la evidencia disponible en el repositorio; lo que no tiene evidencia figura como «Sin evidencia» y debe ser confirmado por su responsable antes de dar el informe por cerrado. |

> Este informe compara el cronograma base (JJT-GPI-07 v1.2) con lo que el repositorio permite verificar al 03/11/2026. No asume avances que no estén documentados: cada «Sin evidencia» es un punto a confirmar o corregir por el responsable de la actividad.

## **1. Resumen ejecutivo**

*Semáforo según Plan de Comunicaciones (JJT-GPI-11).*

| Dimensión | Estado | Comentario |
| :---- | :---- | :---- |
| Plazo | **Rojo** | Estamos en la semana 12 (sprint S3, hito H2). H1 no está cerrado: falta el spike 2.3, que era de las semanas 4–6. |
| Alcance | Amarillo | Sin cambios aprobados. No hay evidencia de funcionalidad construida de H2. |
| Calidad | Amarillo | Los planes de prueba de 3.5 y 4.7 no existían; se emiten con este informe (`qa/PlanPruebas-H2.md`). |
| Riesgos | **Rojo** | R1 (complejidad de ARCA) tiene su disparador cumplido desde el 27/09/2026. |
| Costo / horas | Sin dato | No hay registro de horas por integrante en el repositorio (ver §5). |

## **2. Avance contra el cronograma base**

Al cierre de la semana 11 (01/11/2026) el cronograma prevé **17 de 48 actividades terminadas**: 1.1–1.5, 2.1–2.4, 3.1–3.4 y 4.1.1–4.2.

| Paquete | Previsto terminado al 01/11 | Evidencia en el repositorio | Estado |
| :---- | :---- | :---- | :---- |
| 1.0 Gestión | 1.1, 1.2, 1.3, 1.4, 1.5 | Documentos JJT-GPI-01 a 13 | Completo (1.5 con retraso: sem. 8 en vez de 2–5) |
| 2.0 Diseño | 2.1, 2.2, 2.3, 2.4 | JJT-GPI-14, 15, 16 | 3 de 4. **2.3 spike ARCA: abierto** |
| 3.0 Productos y Stock | 3.1, 3.2, 3.3, 3.4 | `frontend/` solo contiene CLAUDE.md y deuda técnica | **Sin evidencia** |
| 4.0 Facturación | 4.1.1, 4.1.2, 4.1.3, 4.2 | `backend/` solo contiene CLAUDE.md y deuda técnica | **Sin evidencia** (además depende de 2.3) |

**Resultado verificable: 8 de 17 actividades previstas (47%).** Si el código existe fuera de este repositorio, el avance real es mayor y debe incorporarse al informe.

En curso esta semana según el cronograma: 4.3 Notas de Crédito/Débito (sem. 11–12), 4.4 Errores y logging (sem. 12–13) y 4.7 Pruebas de integración ARCA (sem. 12–15). 3.5 arranca en la semana 13.

## **3. Hitos**

| Hito | Fecha objetivo | Estado |
| :---- | :---- | :---- |
| H1 | 27/09/2026 | **No cumplido.** Revisión de hito realizada con resultado negativo: ver JJT-GPI-18. |
| H2 | 29/11/2026 | **En riesgo alto.** Quedan 4 semanas y el paquete de Facturación (ruta crítica) no tiene evidencia de inicio. |
| H3 | 24/01/2027 | Sin cambios por ahora; depende de recuperar H2. |
| H4 | 21/02/2027 | Sin cambios por ahora. |

## **4. Impacto en la ruta crítica**

El Cronograma §5 deja una única semana de margen (26 semanas lógicas contra 27 del plan). La ruta crítica nace en el spike 2.3 → 4.1.1 → … → 4.4. Si el spike se cierra recién en la semana 13, la cadena 4.1.1–4.4 (9 semanas) llevaría su fin a la semana 22 en lugar de la 14, y el resto de la ruta (6.x, 7.x, 9.x, ≈13 semanas) a la semana 35, es decir **unas 8 semanas más que el plan (fin hacia mediados de abril de 2027)**, salvo que se paralelicen actividades, se use la reserva o se recorte alcance. Es una estimación de orden de magnitud y debe recalcularse en el control de cambios.

## **5. Riesgos y problemas**

| ID | Riesgo / problema | Estado al 03/11/2026 | Acción propuesta | Responsable |
| :---- | :---- | :---- | :---- | :---- |
| R1 | Complejidad de los WS de ARCA | **Materializado**: el disparador (sin CAE al cierre de la sem. 6) se cumplió el 27/09/2026. | Ejecutar el spike 2.3 de inmediato; si en 5 días hábiles no hay CAE, aplicar la contingencia del Plan de Riesgos (librería de terceros y replanificación de H2 por control de cambios). | Tomás |
| R5 / R10 | Capacidad y dedicación parcial del equipo | Probable: el atraso acumulado supera la capacidad de 40 h/semana. | Medir horas reales por integrante desde esta semana. | Tomás |
| P-1 | No hay registro de horas, SPI ni CPI desde el último informe (observación 17 del Plan de Proyecto, abierta). | Problema abierto. | Registrar horas semanales y calcular SPI/CPI en el próximo informe. | Todos |
| P-2 | Informes de las semanas 9 a 11 no emitidos. | Problema abierto. | Este informe los consolida. | Jesus |

## **6. Aseguramiento de calidad (QA/QC)**

- Emitidos: Registro de Revisión de Pares (JJT-GPI-13), Revisión del Modelo de Datos (JJT-GPI-16), este informe y el Acta de Revisión de H1 (JJT-GPI-18).
- Emitido: **Plan de Pruebas de H2** (`qa/PlanPruebas-H2.md`) con los casos PC-STK y PC-ARCA, listos para ejecutarse cuando existan los módulos.
- Deuda técnica: sin ítems registrados (no hay código que revisar).
- Defectos abiertos: 0 (no hay software para probar).

## **7. Decisiones requeridas**

1. **Tomás (Director):** fecha comprometida para cerrar el spike 2.3 y confirmar si el código de 3.x y 4.x existe fuera del repositorio.
2. **Tomás y el Sponsor:** si el spike no cierra en la semana 13, abrir control de cambios (Alcance §7) para replanificar H2–H4 o recortar alcance.
3. **Equipo:** desde la semana 13, commits del código en este repositorio y registro semanal de horas.

## **8. Próximos pasos (semanas 13 y 14)**

| Acción | Responsable | Fecha |
| :---- | :---- | :---- |
| Spike 2.3: conexión a homologación y CAE de una factura de prueba | Tomás | 10/11/2026 |
| Confirmar y subir al repositorio el avance de 3.1–3.4 | Juan | 06/11/2026 |
| Ejecutar PC-STK parcial sobre lo disponible (3.5) | Jesus | desde 09/11/2026 |
| Preparar entorno y datos de PC-ARCA (4.7) y ejecutar al cerrar 4.3 | Jesus con Tomás | desde 09/11/2026 |
| Informe de Estado semana 14 con SPI/CPI y horas reales | Jesus | 17/11/2026 |
