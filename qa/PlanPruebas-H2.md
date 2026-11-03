# Plan de Pruebas H2 — Productos y Stock (PC-STK) y Facturación ARCA (PC-ARCA)

**Responsable:** Jesus Manuel Martinez (QA y QC) · **Versión:** 1.0 · **Fecha:** 03/11/2026
**Actividades:** 3.5 (PC-STK) y 4.7 (PC-ARCA) · **Hito:** H2 (29/11/2026)
**Referencias:** Plan de Calidad (JJT-GPI-10) §4–§7; Requerimientos RF-01 a RF-11, RNF-04, 05, 09.

**Estado:** casos diseñados, **sin ejecutar** (los módulos aún no están disponibles en el repositorio). La columna «Resultado» se completa al ejecutar; no se asume ningún resultado.

## 1. Criterios

- **Entrada PC-STK:** 3.1–3.4 integradas en la rama de integración, con datos de ejemplo.
- **Entrada PC-ARCA:** spike 2.3 cerrado (CAE de homologación), 4.2 y 4.3 integradas, CUIT y certificado de testing por variable de entorno (nunca versionados).
- **Salida (compuerta H2):** PC-STK y PC-ARCA aprobadas, CAE en homologación para A/B/C y NC/ND, 0 defectos críticos, 0 secretos en repositorio y logs.
- Defectos: severidad y flujo del Plan de Calidad §6. Se registran en `qa/` con requerimiento afectado, pasos y responsable.

## 2. Casos PC-STK (actividad 3.5)

| ID | Req. | Caso | Resultado esperado | Resultado |
| :---- | :---- | :---- | :---- | :---- |
| STK-01 | RF-01 | Alta de producto con todos los datos obligatorios | Se crea y aparece en el listado | — |
| STK-02 | RF-01 | Alta sin código, descripción o precio | Rechazo con mensaje por campo faltante | — |
| STK-03 | RF-01 | Modificación de precio y descripción | Cambios persistidos | — |
| STK-04 | RF-01 | Baja de producto | Deja de estar disponible para venta; el historial se conserva | — |
| STK-05 | RF-01 | Código de producto duplicado | Rechazo | — |
| STK-06 | RF-02 | Crear categorías de dos rubros distintos (kiosco, indumentaria) | Se crean sin categorías fijas preexistentes | — |
| STK-07 | RF-03 | Definir atributos de variante (talle, color, presentación) por configuración | Variantes creadas sin cambios de esquema ni de código | — |
| STK-08 | RF-03 | Producto con variantes múltiples | Stock independiente por variante | — |
| STK-09 | RF-04 | Consultar stock actual por producto/variante | Valor coherente con los movimientos | — |
| STK-10 | RF-04 | Ajuste manual con motivo | Stock actualizado y motivo registrado | — |
| STK-11 | RF-04 | Ajuste sin motivo | Rechazo | — |
| STK-12 | RF-04 | Ajuste que dejaría stock negativo | Rechazo o advertencia, según lo definido por el Director | — |
| STK-13 | RF-05 | Configurar stock mínimo y bajar el stock por debajo | Aparece una alerta visible | — |
| STK-14 | RF-05 | Reponer el stock sobre el mínimo | La alerta desaparece | — |
| STK-15 | RNF-03 | Regresión de configuración | Cambios de categorías/variantes sin tocar código | — |

## 3. Casos PC-ARCA (actividad 4.7)

Ambiente: homologación de ARCA con CUIT de prueba. Se guarda como evidencia el CAE devuelto y los logs sin datos sensibles.

| ID | Req. | Caso | Resultado esperado | Resultado |
| :---- | :---- | :---- | :---- | :---- |
| ARCA-01 | RF-08 | Autenticación WSAA con certificado de homologación | Token/Sign obtenidos | — |
| ARCA-02 | RF-08 | Reuso del ticket vigente y renovación antes del vencimiento | No hay reautenticación innecesaria; renovación transparente | — |
| ARCA-03 | RF-06 | Factura A con IVA discriminado | CAE obtenido y comprobante persistido | — |
| ARCA-04 | RF-06 | Factura B | CAE obtenido | — |
| ARCA-05 | RF-06 | Factura C | CAE obtenido | — |
| ARCA-06 | RF-06 | Comprobante con múltiples alícuotas de IVA | Totales e IVA correctos | — |
| ARCA-07 | RF-07 | Nota de Crédito asociada a una factura | CAE obtenido; referencia al original | — |
| ARCA-08 | RF-07 | Nota de Débito asociada a una factura | CAE obtenido; referencia al original | — |
| ARCA-09 | RF-09 | Error simulado de WS (rechazo) | Error mostrado y registrado; no se asume CAE | — |
| ARCA-10 | RF-09 | Servicio de ARCA no disponible o timeout | Falla controlada; el comprobante queda pendiente de reintento | — |
| ARCA-11 | RF-10, RNF-05 | Revisión de logs de las pruebas anteriores | Sin certificados, claves, tokens ni CUIT reales | — |
| ARCA-12 | RNF-04 | Escaneo de secretos del repositorio (archivos .crt/.key, CUIT y claves) | 0 hallazgos | — |
| ARCA-13 | RF-08, RNF-09 | Cambio de ambiente homologación ↔ producción solo por variable de entorno | Sin cambios de código; por defecto homologación | — |
| ARCA-14 | RF-11 | Exportar comprobante a PDF | Incluye datos fiscales, ítems, IVA y CAE | — |
| ARCA-15 | CE-1 | Resumen de evidencia de A/B/C y NC/ND | 5 de 5 tipos con CAE | — |

## 4. Cronograma de ejecución

| Actividad | Cuándo | Condición |
| :---- | :---- | :---- |
| Preparar entorno y datos de ejemplo de dos rubros | Semana 13 | Rama de integración disponible |
| PC-STK | Semanas 13–15 (actividad 3.5) | 3.4 y 3.2 integradas |
| PC-ARCA (ARCA-01 a ARCA-10) | Desde la semana 12 (actividad 4.7), al cerrar 4.3 | Spike 2.3 cerrado |
| PC-ARCA (ARCA-11 a ARCA-15) y regresión | Semana 15 | 4.4 y 4.6 integradas |

## 5. Riesgos para la ejecución

- Sin spike 2.3 no se puede ejecutar PC-ARCA (R1 materializado; ver JJT-GPI-17 y JJT-GPI-18).
- Si 3.x y 4.x llegan juntas en la semana 15, el tiempo de las pruebas (hoy 4 semanas combinadas) y de la corrección de defectos queda por debajo de lo necesario para cerrar H2.
