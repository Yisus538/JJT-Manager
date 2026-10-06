JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Plan de Gestión de Riesgos**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-09 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Horizonte | 27 semanas (19/08/2026 – 21/02/2027) |
| Fecha / Versión / Estado | 06/10/2026 · 1.1 · Borrador para revisión |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 05/10/2026 | Emisión inicial (borrador). |
| 1.1 | 06/10/2026 | Pasa a formato Markdown. La reserva de 110 h se asigna por prioridad y deja de superar lo disponible: la exposición no cubierta (37,2 h) queda declarada y con tratamiento explícito. R10 se reformula como "dedicación parcial del equipo". Se corrige el nivel de R1 y R2 ("alto", no "crítico"), el disparador de R6 (alineado al semáforo del Plan de Comunicaciones), la mitigación de R3 y las referencias cruzadas. Se eliminan citas bibliográficas internas. |

> Plan de gestión de riesgos. Amplía los dos riesgos de alto nivel del Acta de Constitución y del Documento de Alcance (§5) hasta un registro completo, con análisis cualitativo (probabilidad × impacto), análisis cuantitativo (VME) y plan de respuesta, siguiendo el proceso planificar → identificar → analizar → responder → monitorear. Un riesgo se expresa como causa → evento → efecto.

**11** amenazas + 1 oportunidad · **147 h** (USD 3.680) VME total de amenazas · **110 h** reserva disponible (USD 2.750) · **12** nivel máximo (R1 y R2, "alto")

## **1. Escalas de probabilidad e impacto**

Las escalas se calibran a este proyecto: el impacto se expresa en horas adicionales de esfuerzo, valorizadas a USD 25/h (Acta). Nivel de riesgo = Probabilidad × Impacto.

| Nivel P | Probabilidad | Rango | Valor usado en VME |
| :----: | :---- | :---- | :----: |
| 1 | Muy baja | < 10% | 5% |
| 2 | Baja | 10–30% | 20% |
| 3 | Media | 31–50% | 40% |
| 4 | Alta | 51–70% | 60% |
| 5 | Muy alta | > 70% | 80% |

| Nivel I | Impacto | Esfuerzo adicional | Efecto sobre el proyecto |
| :----: | :---- | :---- | :---- |
| 1 | Bajo | < 10 h | Sin efecto en hitos |
| 2 | Moderado | 10–25 h | Absorbible por la holgura de una actividad |
| 3 | Significativo | 26–50 h | Puede consumir la holgura de un hito |
| 4 | Alto | 51–80 h | Amenaza la fecha de un hito |
| 5 | Crítico | > 80 h | Amenaza la fecha final o un criterio de éxito |

## **2. Matriz de evaluación probabilidad × impacto**

*Nivel = P × I. Clasificación: 1–4 bajo · 5–9 medio · 10–14 alto · 15–25 crítico.*

| | I=1 | I=2 | I=3 | I=4 | I=5 |
| :----: | :----: | :----: | :----: | :----: | :----: |
| **P=5** | 5 | 10 | 15 | 20 | 25 |
| **P=4** | 4 | 8 — R10 | 12 — **R2** | 16 | 20 |
| **P=3** | 3 | 6 | 9 — R6, R11 | 12 — **R1** | 15 |
| **P=2** | 2 | 4 — R9 | 6 — R3, R4, R8 | 8 — R7 | 10 — R5 |
| **P=1** | 1 | 2 | 3 | 4 | 5 |

## **3. Registro de riesgos**

*11 amenazas · 1 oportunidad.*

| ID | Riesgo (causa → evento → efecto) | Categoría | P | I | Nivel | Resp. | EDT · Hito | Origen |
| :---- | :---- | :---- | :----: | :----: | :----: | :---- | :---- | :---- |
| R1 | Si la documentación de los WS de ARCA es insuficiente o compleja, la integración WSAA/WSFEv1 se demorará y retrasará la ruta crítica (4.0). | Técnico / externo | 3 | 4 | 12 | Tomás | 2.3, 4.x · H1–H2 | Acta — Riesgos; Alcance §5 |
| R2 | Si el dominio multirubro invita a pedidos no controlados, el alcance crecerá (scope creep) y se generará retrabajo y desvío de hitos. | Alcance / gestión | 4 | 3 | 12 | Tomás | Todas · H1–H4 | Acta — Riesgos; Alcance §5 y §7 |
| R3 | Si el ambiente de homologación de ARCA no está disponible o es inestable (supuesto del Acta), las pruebas de facturación se bloquearán. | Externo | 2 | 3 | 6 | Tomás | 4.x, 9.3 · H2, H4 | Acta — Supuestos; Alcance §6 |
| R4 | Si no se dispone de una CUIT de prueba con certificados de testing (supuesto del Acta), el spike y la facturación no podrán iniciarse. | Externo | 2 | 3 | 6 | Tomás | 2.3 · H1 | Acta — Supuestos; RNF-09 |
| R5 | Si un integrante del equipo fijo (RNF-10) queda indisponible, se perderá conocimiento y capacidad sin posibilidad de reemplazo. | Recursos | 2 | 5 | 10 | Tomás | Todas · H1–H4 | Acta — Restricciones; RNF-10 |
| R6 | Si la estimación subestima el esfuerzo (H2 está al 101% de su capacidad), se agotará la reserva y se desviarán fechas. | Estimación | 3 | 3 | 9 | Tomás | 3.0, 4.0 · H2 | Estimación y Presupuesto §5 |
| R7 | Si se versionan certificados, claves o CUIT reales, o se escriben en los logs, se expondrán credenciales de ARCA. | Seguridad | 2 | 4 | 8 | Tomás | 4.4, 4.6, 4.7 · H2 | RNF-04, RNF-05; RF-10 |
| R8 | Si el modelo de datos asume lógica de un rubro específico, no se cumplirá la genericidad (RF-32) y habrá que rediseñar. | Técnico / alcance | 2 | 3 | 6 | Tomás | 2.2, 2.4, 9.2 · H1, H4 | RNF-01 a 03; RF-32 |
| R9 | Si ARCA modifica la normativa o sus WS durante el desarrollo, será necesario adaptar la integración. | Externo | 2 | 2 | 4 | Tomás | 4.x · H2 | Acta — Interesados (ARCA) |
| R10 | Si el equipo tiene dedicación parcial al proyecto (13,3 h/semana por integrante) y la disponibilidad real baja en ciertas semanas, se atrasarán actividades. | Recursos | 4 | 2 | 8 | Tomás | Todas · H1–H4 | Estimación y Presupuesto §5 |
| R11 | Si las pruebas se concentran en H4, los defectos críticos se detectarán tarde y consumirán la holgura final. | Calidad | 3 | 3 | 9 | Jesus | 9.x · H4 | Lista de Actividades 9.0; Plan de Calidad |
| R12 | **Oportunidad:** si se encuentra una librería de terceros probada para WSAA/WSFEv1, se reducirá el esfuerzo de 4.1.x. | Oportunidad | 3 | 3 | 9 | Tomás | 4.1.x · H2 | Acta — Riesgos (estrategia inicial) |

*Los riesgos R1 y R2 provienen del Acta de Constitución y del Documento de Alcance (§5); R3 y R4 de los supuestos del Acta; R5 de la restricción RNF-10; R7 y R8 de RNF-04/05 y RF-32; R6, R10 y R11 del análisis de capacidad y del plan de pruebas de este lote de documentos. R12 es una oportunidad (efecto positivo) y no suma exposición. Los riesgos R6, R10 y R11 se proponen para ser incorporados a la sección de riesgos del Documento de Alcance (§5) en su próxima versión.*

## **4. Análisis cuantitativo (VME)**

*Valor monetario esperado: VME = probabilidad × impacto monetario. Es una referencia de exposición, no un gasto previsto.*

| Riesgo | Impacto | Prob. | VME (USD) | VME (h) |
| :---- | :----: | :----: | :----: | :----: |
| R1 | $1.500 (60 h) | 40% | $600 | 24,0 |
| R2 | $1.000 (40 h) | 60% | $600 | 24,0 |
| R5 | $2.500 (100 h) | 20% | $500 | 20,0 |
| R11 | $1.000 (40 h) | 40% | $400 | 16,0 |
| R10 | $600 (24 h) | 60% | $360 | 14,4 |
| R6 | $750 (30 h) | 40% | $300 | 12,0 |
| R7 | $1.500 (60 h) | 20% | $300 | 12,0 |
| R8 | $1.000 (40 h) | 20% | $200 | 8,0 |
| R3 | $750 (30 h) | 20% | $150 | 6,0 |
| R4 | $750 (30 h) | 20% | $150 | 6,0 |
| R9 | $600 (24 h) | 20% | $120 | 4,8 |
| R12 | +$1.000 (40 h) | 40% | +$400 | oportunidad |
| **Total amenazas** | | | **$3.680** | **147,2** |

**Comparación con la reserva.** La exposición esperada ($3.680; 147,2 h) supera en $930 (37,2 h) la reserva de 110 h ($2.750) definida en el presupuesto (Estimación y Presupuesto, §6). Los cuatro riesgos de mayor VME (R1, R2, R5, R11) concentran el 57% de la exposición. Además, la holgura de capacidad del proyecto (110 h) es la misma reserva (Estimación y Presupuesto §5), por lo que **la reserva no puede asignarse a todos los riesgos**. Decisión de gestión:

1. La reserva de 110 h se asigna por prioridad de VME a R1, R2, R5, R11, R10 y R6 (24 + 24 + 20 + 16 + 14 + 12 = 110 h). Ver la columna "Reserva (h)" de §5.
2. Los riesgos R7, R8, R3, R4 y R9 (VME 36,8 h; la exposición sin cubrir es de 37,2 h por el redondeo a 14 h de R10) **no tienen reserva asignada**: se tratan con acciones preventivas de costo bajo o nulo y, si alguno se materializa, el Director de Proyecto solicita al Sponsor reserva de gestión mediante el proceso de control de cambios (Alcance §7).
3. Las respuestas de §5 buscan reducir la probabilidad antes de consumir reserva.
4. Si el consumo supera el 80% de la reserva, se eleva al Sponsor.

## **5. Plan de respuesta**

*Estrategia, disparador y contingencia.*

| ID | Estrategia | Acciones preventivas | Disparador | Contingencia | Reserva (h) | Residual / secundario |
| :---- | :---- | :---- | :---- | :---- | :----: | :---- |
| R1 | Mitigar | Spike técnico de homologación (2.3) en sem. 4–6; evaluar librerías de terceros probadas; validar WSAA/WSFEv1 antes de comprometer H2. | Spike 2.3 sin CAE de homologación al cierre de la sem. 6. | Adoptar librería/adaptador de terceros y reasignar reserva de H1/H2; replanificar H2 por control de cambios. | 24 | Residual: cambios de contrato del WS. Secundario: dependencia de una librería externa. |
| R2 | Evitar / mitigar | Aplicar el proceso formal de control de cambios (Alcance §7); registrar todo pedido por escrito y medir su impacto antes de aceptarlo. | Pedido que modifica un ítem incluido/excluido sin registro de cambio. | Rechazar o diferir el pedido; si es significativo, aprobación explícita del Sponsor y re-estimación. | 24 | Residual: pedidos informales fuera del circuito. |
| R3 | Aceptar (activa) | Aislar el cliente WS tras una interfaz que permita simular respuestas; avanzar con el módulo Productos y Stock (3.0), el único de H2 sin dependencia de ARCA, durante cortes de servicio. | Más de 2 días hábiles sin respuesta del ambiente de homologación. | Trabajar contra respuestas simuladas y repetir la validación real al restablecerse el servicio. | — | Secundario: la simulación puede ocultar diferencias reales con ARCA. |
| R4 | Mitigar | Gestionar CUIT de prueba y certificados de testing durante las sem. 1–3, antes de iniciar 2.3. | Sin certificado de testing al inicio de la sem. 4. | Escalar al Sponsor; reorganizar el spike hacia tareas de diseño y modelo de datos mientras se obtiene el certificado. | — | Residual: demora del trámite fuera del control del equipo. |
| R5 | Mitigar / aceptar | Documentar decisiones técnicas, trabajar en pares en 4.0 y mantener repositorio y documentación compartidos; reparto cruzado de tareas de QA (actividades de QA por módulo, Lista v1.1). | Ausencia de un integrante superior a 2 semanas. | Redistribuir actividades entre los dos integrantes restantes y proponer, vía control de cambios, el ajuste de alcance o fechas. | 20 | Residual: capacidad reducida. Secundario: sobrecarga del resto del equipo. |
| R6 | Mitigar | Registrar horas reales por actividad cada semana y comparar con la línea base; recalibrar al cierre de H2. | SPI o CPI en rojo (< 0,85) durante 2 semanas seguidas, o consumo de reserva > 50% antes del cierre de H2. | Re-estimar el trabajo restante y proponer reasignación de reserva o ajuste de alcance. | 12 | Residual: falta de datos históricos propios. |
| R7 | Evitar / mitigar | Variables de entorno y archivos ignorados por git (.crt, .key, .env); escaneo de secretos antes de cada integración; revisión de logs en las pruebas de 4.4 y 4.7. | Hallazgo de un secreto en el repositorio o en un log. | Revocar y regenerar certificados, reescribir el historial afectado y registrar el incidente. | — | Residual: error humano. Secundario: interrupción por rotación de certificados. |
| R8 | Mitigar | Validar el modelo de datos contra dos rubros de ejemplo (kiosco e indumentaria) ya en 2.2 y 2.4; atributos y categorías configurables, sin columnas fijas. | Un rubro de ejemplo que exija cambios en el esquema o en el código. | Refactorizar el módulo afectado hacia parámetros de configuración antes del cierre de H2. | — | Residual: casos de rubros no contemplados. |
| R9 | Aceptar / mitigar | Parametrizar IVA y tipos de comprobante (RNF-03); seguimiento periódico de los comunicados oficiales de ARCA. | Comunicado oficial de ARCA que afecte a WSAA/WSFEv1. | Analizar el impacto y registrar un cambio si afecta fechas o alcance. | — | Residual: cambios sin aviso previo. |
| R10 | Mitigar | Planificar sobre 40 h/semana del equipo; acordar con anticipación las semanas de menor disponibilidad y nivelar la carga (Cronograma §6). | Horas reales de la semana inferiores al 75% de la capacidad (30 h). | Reprogramar actividades con holgura y avisar al Sponsor si se afecta un hito. | 14 | Residual: semanas pico no nivelables (H2 al 101%). |
| R11 | Mitigar | Pruebas por módulo al cierre de cada hito (Plan de Calidad §3 y §7), ya programadas como actividades 3.5, 4.7, 5.4, 6.5, 7.7 y 8.3; regresión continua; QA transversal desde H1 (1.5, 2.4). | Más de 1 defecto crítico abierto al cierre de un hito. | Detener nuevas funcionalidades hasta corregir; usar la holgura de H4 (30 h). | 16 | Residual: defectos de integración tardíos. |
| R12 | Explotar | Evaluar librerías candidatas durante el spike 2.3 y decidir antes de iniciar 4.1.1. | Librería aprobada en el spike. | — | — | Secundario: dependencia externa (ver R1). |

*Estrategias para amenazas: evitar, transferir, mitigar o aceptar; para oportunidades: explotar, compartir, mejorar o aceptar. No se prevé transferir riesgos a terceros (no hay seguros ni contratos de servicio con penalidades en el alcance). Reserva (h) = VME redondeado; suma asignada = 110 h; "—" = sin reserva asignada (ver §4).*

## **6. Monitoreo y control de riesgos**

| Actividad | Frecuencia | Responsable | Registro / criterio |
| :---- | :---- | :---- | :---- |
| Revisión del registro de riesgos (probabilidad, impacto, nivel, responsable) | Quincenal; semanal durante H2 | Tomás Disandro | Registro actualizado; acta de la reunión de coordinación |
| Verificación de ejecución y eficacia de las respuestas; riesgos residuales | En cada revisión | Responsable de cada riesgo | Estado de la acción y evidencia |
| Identificación de nuevos riesgos (brainstorming, análisis de supuestos) | En cada cierre de hito | Equipo | Nuevas filas en el registro |
| Cierre de riesgos | Al vencer la ventana de exposición | Responsable + Director | Cierre con evidencia |
| Materialización: el riesgo pasa a gestionarse como incidente/problema | Por evento | Director de Proyecto | Acción correctiva verificable (Plan de Comunicaciones y Seguimiento, §6) |
| Consumo de reserva: alerta al 50% y escalamiento al Sponsor al 80% | Mensual | Director de Proyecto | Reserva consumida / 110 h |
