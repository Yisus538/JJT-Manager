JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Registro de Revisión de Pares (actividad 1.5)**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-13 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Revisor | Jesus Manuel Martinez (QA y QC) |
| Fecha / Versión / Estado | 07/10/2026 · 1.0 · Completada |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 07/10/2026 | Emisión inicial: cierre de la actividad 1.5 con la lista de observaciones de la revisión del 06–07/10/2026 y su resolución. |

> Registro de la actividad 1.5 (Lista de Actividades v1.2): revisión de pares de los documentos de gestión (consistencia entre documentos, trazabilidad RF/RNF → EDT → hito y ortografía). La lista de observaciones resueltas es requisito de la compuerta H1 (Plan de Calidad §7). La actividad estaba prevista en las semanas 2–5 y se ejecutó en la semana 8.

## **1. Alcance de la revisión**

Documentos revisados: Acta de Constitución (01), Registro de Interesados (02), Requerimientos (03), Alcance y Gestión (04), EDT (05), Lista de Actividades (06), Cronograma (07), Estimación y Presupuesto (08), Plan de Riesgos (09), Plan de Calidad (10), Plan de Comunicaciones (11) y Plan de Proyecto (12). Método: cruce de cada dato (fechas, horas, precedencias, responsables, umbrales, referencias RF/RNF) entre documentos, recálculo del CPM y de las horas por rol, y verificación contra el contenido del repositorio.

## **2. Observaciones y resolución**

*Estado: Resuelta = corregida en los documentos vigentes; Declarada = el problema se documentó con su tratamiento; Abierta = requiere una decisión o evidencia pendiente.*

| N.º | Observación | Documento(s) | Estado | Resolución |
| :----: | :---- | :---- | :---- | :---- |
| A1 | Metodología con «[N]» sin definir; ningún documento reflejaba sprints. | 01, 07, 10, 11, 12 | Resuelta | Sprints de 2 semanas (Acta v1.2); calendario S1–S8 en Cronograma §2; revisión de sprint en Comunicaciones; backlog de defectos y sprints en Calidad §4 (v1.2). |
| A2 | El presupuesto del Acta no reflejaba las 970 h de línea base ni la reserva de 110 h. | 01 | Resuelta | Acta v1.3 §8: USD 27.000 es el techo, con 970 h (USD 24.250) más 110 h (USD 2.750). |
| A3 | El objetivo 6 hablaba de reportes de clientes y medios de pago, fuera del alcance. | 01 | Resuelta | Acta v1.3: el objetivo 6 lista los cinco reportes del alcance. |
| A4 | Interesados: faltaba Railway; el comerciante «hipotético» chocaba con las demos de Comunicaciones. | 01, 11 | Resuelta | Railway agregado (Acta v1.2). El comerciante lo cubre una persona a designar por el Sponsor (Acta v1.3, Comunicaciones v1.2). |
| A5 | Formato: viñetas sin anidar, importes con formatos mezclados, título del total, doble espacio. | 01 | Resuelta | Acta v1.3: listas anidadas, importes en formato USD, título «Costos totales (personal e infraestructura)». |
| B1 | 4.6 (credenciales de producción) en la ruta crítica y predecesora de 5.1 y 6.1.2, aunque el Acta las limita a la validación final opcional. | 06, 07, 10 | Resuelta | Lista y Cronograma v1.2: 5.1 y 6.1.2 dependen de 4.4; 4.6 antecede a 9.3. |
| B2 | «Cronograma base aprobado» con el documento en borrador. | 07 | Resuelta | Redacción corregida en el Cronograma v1.1; la aprobación del Sponsor quedó registrada el 07/10/2026. |
| B3 | Criterios de entrada de H1 y H2 sin cumplir y no registrados. | 10 | Declarada | Calidad §7 v1.2: entrada de H1 sin afirmar aprobación; nota de estado de la compuerta H1 (Plan de Proyecto §5, obs. 9). R4 quedó confirmado. |
| B4 | Definición inconsistente del resultado del spike 2.3. | 06, 07, 09, 10 | Resuelta | En todos los documentos el spike exige conexión documentada y CAE de homologación de una factura de prueba. |
| B5 | Disparador de R4 vencido sin contingencia ni escalamiento. | 09 | Resuelta | Plan de Riesgos v1.2: estado registrado; R4 confirmado el 07/10/2026. |
| B6 | Umbral de R6 (0,90) distinto del semáforo de Comunicaciones. | 09, 11 | Resuelta | Alineados en < 0,85 durante 2 semanas (Riesgos v1.1). |
| B7 | R10 hablaba de «obligaciones académicas», sin respaldo en el Acta. | 09 | Resuelta | R10 reformulado como «dedicación parcial del equipo» (Riesgos v1.1). |
| B8 | La gestión continua y los documentos 07–12 no tienen horas; las 60 h de 1.0 se consumen en 1.1–1.5. | 08, 05, 06 | Abierta | Declarado en Estimación v1.2 §7 y Plan de Proyecto obs. 17. Falta decidir cómo financiarlo (actividad nueva con re-estimación o reserva). |
| B9 | Horas por rol inconsistentes entre Estimación §3 y §4 (Jesus 370 h; Juan 265 h). | 08, 06 | Resuelta | Estimación v1.2 §4: 63 h de apoyo entre integrantes; carga 323/324/323 h. |
| C1 | El ejemplo de acción correctiva atribuía el pico a actividades que no coinciden. | 11, 07 | Resuelta | Ejemplo rehecho sobre las semanas 13–14 (Comunicaciones v1.2). |
| C2 | Indicador de verificación de ≤ 50 h frente a una capacidad de 40 h. | 11 | Resuelta | Indicador «≤ 50 h (verde ≤ 40)», coherente con el semáforo. |
| C3 | CPM: cadenas de actividades de 1 semana colapsadas; «18 semanas lógicas» poco fiables. | 07 | Resuelta | CPM recalculado con una convención que no colapsa cadenas: 26 semanas lógicas (Cronograma v1.2). |
| C4 | Reportes 7.x y roles 8.x encadenados en serie sin dependencia lógica. | 06 | Resuelta | Lista v1.2: precedencias por datos consumidos; el orden en serie del calendario se declara como restricción de recurso. |
| C5 | Matriz de trazabilidad: facturación sin H4/9.3 y cuatro filas sin riesgos. | 12 | Resuelta | Plan de Proyecto v1.2 §4. |
| D1 | Observaciones 3, 5 y 7 del Plan de Proyecto ya resueltas en el Acta. | 12 | Resuelta | Estado actualizado (Plan de Proyecto v1.1). |
| D2 | Faltantes 9, 10 y 12 de los documentos de seguimiento desactualizados. | Seguimiento | Sin objeto | Los PDF de seguimiento se eliminaron del repositorio; sus faltantes se cubren con el Plan de Proyecto §5. |
| D3 | Ubicaciones (.docx, Drive) distintas del repositorio. | 10, 12 | Resuelta | Todos los documentos apuntan a los `.md` de `docs/` (Plan de Proyecto v1.1, Calidad v1.1). |
| E1 | Guiones faltantes («RF32», «RNF10», «JJTGPI-10», «JJT-GPI04»). | Varios | Sin objeto | Verificado: los `.md` los tienen correctos; era un artefacto de la extracción de los PDF. |
| E2 | Encabezados con «27 semanas (19/08 – 21/02)» sin aclarar que se cuentan desde el 17/08. | 07 a 12 | Resuelta | Aclaración agregada en los encabezados (v1.2). |

**Resumen:** 24 observaciones. 20 resueltas, 1 declarada, 2 sin objeto y 1 abierta (B8, decisión de financiamiento). La observación B3 depende además del cierre real de 2.1–2.4 (ver §3).

## **3. Resultado de la revisión y efecto sobre la compuerta H1**

- Los documentos 01 a 12 son consistentes entre sí en fechas, horas (970 h de línea base y 110 h de reserva), precedencias, responsables y umbrales.
- **La actividad 1.5 queda completada.** Su salida (la lista de observaciones resueltas) es este registro.
- La compuerta H1 **no puede darse por cumplida** solo con 1.5: faltan las evidencias de 2.1 (stack), 2.2 (modelo de datos), 2.3 (spike con CAE de homologación) y 2.4 (revisión del modelo contra dos rubros), que son entregables técnicos y no se pueden certificar desde la documentación (Plan de Proyecto §5, obs. 9).

## **4. Aprobación**

*La documentación revisada está aprobada por el Sponsor (confirmado por el equipo el 07/10/2026). Firma y fecha de cada persona, a registrar en la tabla.*

| Rol | Nombre | Firma / Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Revisor (QA y QC) | Jesus Manuel Martinez | | |
| Director de Proyecto | Tomás Disandro | | |
| Sponsor | Julio Gutierrez | | |
