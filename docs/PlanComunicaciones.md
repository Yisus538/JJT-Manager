JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Plan de Comunicaciones y Seguimiento**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-11 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Horizonte | 27 semanas (19/08/2026 – 21/02/2027; semanas contadas desde el lunes 17/08/2026) |
| Fecha / Versión / Estado | 07/10/2026 · 1.2 · Borrador para revisión |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 05/10/2026 | Emisión inicial (borrador). |
| 1.1 | 06/10/2026 | Pasa a formato Markdown. La línea base de valor planificado (PV) se recalcula con las 48 actividades de la Lista v1.1 y el calendario nivelado. El ejemplo de acción correctiva se rehace sobre la carga real del cronograma v1.1 (el anterior mezclaba actividades de H2 con H3 y proponía mover actividades sin holgura suficiente). El umbral de la acción correctiva pasa a ser coherente con la regla de ≤ 50 h/semana. Se registra la revisión de la compuerta H1 como pendiente. Se eliminan citas bibliográficas internas. |
| 1.2 | 07/10/2026 | Se corrige la causa raíz del ejemplo de acción correctiva (semana 13: 3.5, 4.4, 4.5 y 4.7; semana 14: 3.5, 4.5, 4.6 y 4.7). El comerciante tipo se alinea con la definición del Acta v1.3. |

> Plan de comunicaciones y seguimiento. Define quién informa qué, a quién, con qué frecuencia y por qué canal, y cómo se compara el avance real con la línea base de plazo y costo para detectar desvíos y actuar a tiempo. Sin datos comparables no hay seguimiento; sin decisiones, el seguimiento se convierte en informe.

## **1. Interesados y estrategia de comunicación**

*Registro de Interesados (STK-01 a 07).*

| ID | Interesado | Cuadrante | Estrategia (Registro de Interesados) | Qué necesita saber |
| :---- | :---- | :----: | :---- | :---- |
| STK-01 | Julio Gutierrez — Sponsor/Cliente | A | Gestionar de cerca | Avance contra hitos, desvíos de plazo y costo, cambios que requieren su aprobación |
| STK-02 | Tomás Disandro — Director y Backend | A | Gestionar de cerca | Todo el estado del proyecto; riesgos y decisiones pendientes |
| STK-03 | Juan Cruz Bulatovich — Frontend | A | Gestionar de cerca | Prioridades, dependencias y cambios que afecten sus módulos |
| STK-04 | Jesus Manuel Martinez — QA/QC | A | Gestionar de cerca | Entregables listos para prueba; criterios de aceptación; defectos |
| STK-05 | Comerciante tipo (usuario final; perfil representativo a designar por el Sponsor) | C | Mantener informado | Funcionalidad disponible y validación de usabilidad |
| STK-06 | ARCA (organismo fiscal) | B | Mantener satisfecho | Se consulta su documentación y comunicados; no recibe informes del proyecto |
| STK-07 | Railway (infraestructura) | D | Monitorear | Estado del servicio y costos (USD 5/mes) |

## **2. Plan de comunicaciones**

*Qué · Quién · Cuándo · Cómo.*

| Información / evento | Audiencia | Frecuencia | Canal | Responsable | Contenido / salida |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Reunión de coordinación | Equipo (STK-02 a 04) | Semanal | Videollamada | Tomás | Avance, bloqueos, riesgos y plan de la semana; acta breve |
| Informe de estado | Sponsor (STK-01) y equipo | Quincenal (semanal en H2) | Documento en el repositorio (`docs/`) | Tomás | Informe de estado (§7): avance, indicadores, riesgos, cambios |
| Revisión de hito | Sponsor y equipo | Sem. 6, 15, 23 y 27 | Reunión + acta de aprobación | Tomás | Verificación de la compuerta del hito (Plan de Calidad §7) |
| Revisión de sprint | Equipo | Cada 2 semanas en H2 y H3 (sprints S1–S8, Cronograma §2) | Reunión de coordinación | Tomás | Demostración del incremento y backlog del sprint siguiente |
| Revisión de riesgos | Equipo | Quincenal (semanal en H2) | Reunión de coordinación | Tomás | Registro de riesgos actualizado (Plan de Riesgos §6) |
| Solicitud de cambio | Sponsor y equipo | Por evento | Registro escrito (Alcance §7) | Quien propone; decide Director o Sponsor | Análisis de impacto y decisión |
| Demostración y validación | Comerciante tipo (STK-05) | Cierre de H2, H3 y H4 | Demostración | Juan | Retroalimentación de usabilidad |
| Comunicados de ARCA | Equipo | Mensual y al inicio de H2 | Sitio oficial de ARCA | Tomás | Cambios normativos o técnicos (riesgo R9) |
| Defectos y pruebas | Equipo | Semanal | Registro de defectos | Jesus | Estado de pruebas y defectos críticos |
| Documentación y versiones | Equipo y Sponsor | Por evento | Repositorio git (`docs/`) | Autor del documento | Versión vigente con tabla de cambios |

*Los canales y frecuencias son una propuesta del equipo para validar con el Sponsor en la revisión de H1; no se identificaron herramientas adicionales en la documentación vigente. Estado al 06/10/2026: la revisión de H1 (semana 6) figuraba para el 27/09/2026 y no hay acta registrada en `docs/`; queda pendiente de realizar o de documentar.*

## **3. Indicadores y umbrales de seguimiento**

*Semáforo.*

| Indicador | Fórmula / definición | Verde | Amarillo | Rojo | Frecuencia |
| :---- | :---- | :----: | :----: | :----: | :---- |
| SPI (plazo) | EV / PV | ≥ 0,95 | 0,85–0,94 | < 0,85 | Semanal |
| CPI (costo) | EV / AC | ≥ 0,95 | 0,85–0,94 | < 0,85 | Semanal |
| Horas reales vs. estimadas por paquete | Horas registradas / horas de la línea base | ≤ 105% | 106–120% | > 120% | Semanal |
| Avance de hito | Actividades completas / actividades del hito | Según cronograma | 1 semana de atraso | ≥ 2 semanas | Semanal |
| Defectos críticos abiertos | Cantidad | 0 | 1 | ≥ 2 | Semanal |
| Carga semanal planificada | Horas planificadas de la semana (Cronograma §6) | ≤ 40 h | 41–50 h | > 50 h | Al replanificar |
| Riesgos de nivel ≥ 12 sin respuesta ejecutada | Cantidad (R1, R2) | 0 | 1 | ≥ 2 | Quincenal |
| Consumo de reserva | Horas de reserva usadas / 110 h | < 50% | 50–80% | > 80% | Mensual |

*EV (valor ganado) = horas de la línea base de las actividades completadas (criterio 0/100); PV (valor planificado) = horas planificadas hasta la fecha de corte; AC (costo real) = horas registradas por los integrantes a USD 25/h. Umbrales propuestos para validación.*

## **4. Ciclo de seguimiento y escalamiento**

1. **Planificar:** qué medir (indicadores de §3) y contra qué (línea base de §5).
2. **Medir:** cada integrante registra las horas reales por actividad antes de la reunión de coordinación semanal.
3. **Comparar:** plan vs. real vs. previsión; el Director calcula SPI, CPI y desvíos por paquete.
4. **Analizar** causas y tendencias cuando un indicador pasa a amarillo; **actuar** (corregir, prevenir o escalar) cuando pasa a rojo.
5. **Verificar:** comprobar el efecto de cada acción en la revisión siguiente.
6. **Escalamiento:** desvío rojo durante 2 semanas, riesgo materializado con impacto en un hito, o consumo de reserva > 80% → el Director informa al Sponsor y, si corresponde, abre una solicitud de cambio (Alcance §7). El disparador del riesgo R6 usa el mismo criterio (SPI o CPI en rojo durante 2 semanas).

## **5. Línea base de seguimiento (valor planificado)**

*Estimación y Presupuesto §6.*

La línea base de seguimiento es el valor planificado (PV) acumulado por semana, obtenido distribuyendo uniformemente las horas esperadas de cada actividad (Estimación y Presupuesto, §3) sobre sus semanas planificadas (Cronograma, §3). Termina en 970 h (USD 24.250 = BAC); la reserva de 110 h se gestiona aparte. Capacidad de referencia: 40 h por semana.

| Sem. | Hito | Horas planificadas | PV acum. (h) | PV acum. (USD) | % de la línea base |
| :----: | :---- | :----: | :----: | :----: | :----: |
| 1 | H1 | 16 | 16 | $400 | 2% |
| 2 | H1 | 32,8 | 48,8 | $1.219 | 5% |
| 3 | H1 | 28,8 | 77,5 | $1.938 | 8% |
| 4 | H1 | 38,1 | 115,6 | $2.890 | 12% |
| 5 | H1 | 24,1 | 139,7 | $3.492 | 14% |
| 6 | H1 | 20,3 | 160 | $4.000 | 16% |
| 7 | H2 | 35,5 | 195,5 | $4.888 | 20% |
| 8 | H2 | 42 | 237,5 | $5.938 | 24% |
| 9 | H2 | 42,3 | 279,8 | $6.996 | 29% |
| 10 | H2 | 32,3 | 312,2 | $7.804 | 32% |
| 11 | H2 | 36,8 | 349 | $8.725 | 36% |
| 12 | H2 | 41,2 | 390,2 | $9.756 | 40% |
| 13 | H2 | 47,8 | 438 | $10.950 | 45% |
| 14 | H2 | 47,8 | 485,8 | $12.144 | 50% |
| 15 | H2 | 39,2 | 525 | $13.125 | 54% |
| 16 | H3 | 25,5 | 550,5 | $13.762 | 57% |
| 17 | H3 | 41,5 | 592 | $14.800 | 61% |
| 18 | H3 | 47 | 639 | $15.975 | 66% |
| 19 | H3 | 40,8 | 679,8 | $16.996 | 70% |
| 20 | H3 | 37,3 | 717,2 | $17.929 | 74% |
| 21 | H3 | 37,8 | 755 | $18.875 | 78% |
| 22 | H3 | 41 | 796 | $19.900 | 82% |
| 23 | H3 | 44 | 840 | $21.000 | 87% |
| 24 | H4 | 22,5 | 862,5 | $21.563 | 89% |
| 25 | H4 | 37,5 | 900 | $22.500 | 93% |
| 26 | H4 | 40 | 940 | $23.500 | 97% |
| 27 | H4 | 30 | 970 | $24.250 | 100% |

## **6. Acciones correctivas**

*Ficha de acción verificable.*

| Campo | Contenido |
| :---- | :---- |
| Desviación | Qué indicador se alejó del objetivo |
| Causa raíz | Por qué ocurrió |
| Acción | Qué se hará y desde cuándo |
| Responsable | Persona asignada |
| Fecha objetivo | Cuándo se espera el efecto |
| Indicador de verificación | Cómo se sabrá que funcionó |
| Seguimiento | Mantener, modificar o escalar |

**Ejemplo verificable** (basado en la carga del Cronograma v1.1, §6):

| Campo | Contenido |
| :---- | :---- |
| Desviación | La demanda semanal planificada llega a 47,8 h en las semanas 13 y 14 frente a una capacidad de 40 h (indicador "Carga semanal" en amarillo). |
| Causa raíz | El cierre de H2 concentra, en la semana 13, 3.5, 4.4, 4.5 y las pruebas de integración 4.7, y en la semana 14, 3.5, 4.5, 4.6 y 4.7. |
| Acción | Diseñar los casos de prueba de 4.7 durante la semana 12 (4.7 arranca en esa semana) para llegar a las semanas 13–14 solo con ejecución, y no abrir actividades nuevas en las semanas 13–14; 4.5 (11 semanas de holgura) pasa a la semana 14 si el avance real lo requiere. |
| Responsable | Tomás Disandro, con Jesus Manuel Martinez |
| Fecha objetivo | Antes del inicio de la semana 13 (09/11/2026) |
| Indicador de verificación | Carga semanal real ≤ 50 h en las semanas 13 y 14 (verde ≤ 40 h) |
| Seguimiento | Revisar en la reunión de coordinación de la semana 12 |

## **7. Informe de estado**

*Contenido mínimo.*

- **Resumen:** estado general (verde/amarillo/rojo) y logros del período.
- **Avance:** actividades completadas y en curso; avance del hito vigente.
- **Indicadores:** SPI, CPI, horas reales vs. línea base, defectos críticos, consumo de reserva.
- **Riesgos e incidentes:** cambios en el registro y estado de las respuestas.
- **Cambios:** solicitudes abiertas y resueltas (Alcance §7).
- **Decisiones requeridas del Sponsor y próximos pasos.**

## **8. Datos históricos y calibración**

- Registrar al cierre de cada hito el tamaño y el esfuerzo estimado y real por paquete.
- Calcular el error relativo |real − estimado| / real y analizar el sesgo (¿se subestima o se sobreestima?).
- Conservar los datos como histórico del equipo y las lecciones aprendidas al cierre (9.4) para calibrar futuras estimaciones.
