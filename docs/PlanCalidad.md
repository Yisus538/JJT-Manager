JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Plan de Calidad y Pruebas**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-10 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Horizonte | 27 semanas (19/08/2026 – 21/02/2027; semanas contadas desde el lunes 17/08/2026) |
| Fecha / Versión / Estado | 07/10/2026 · 1.2 · Aprobado por el Sponsor |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 05/10/2026 | Emisión inicial (borrador). |
| 1.1 | 06/10/2026 | Pasa a formato Markdown. Cada prueba (PC-xxx) se vincula a la actividad de QA que la ejecuta en la Lista v1.1 (1.5, 2.4, 3.5, 4.7, 5.4, 6.5, 7.7, 8.3). El criterio de entrada de H1 deja de afirmar que el Acta está aprobada (la aprobación está pendiente). PC-NF pasa a cubrir también RNF-10. Los documentos se versionan en el repositorio git (`docs/`), no en Drive. Se eliminan citas bibliográficas internas. |
| 1.2 | 07/10/2026 | Se alinea el resultado del spike 2.3 con el Plan de Riesgos (R1): conexión a homologación documentada y CAE de homologación obtenido. Se registra el estado de la compuerta H1 y la entrada de H2 (R4 confirmado). Se vincula la estrategia de pruebas con los sprints S1–S8 (backlog de defectos y revisión de sprint). |

> Plan de calidad y pruebas. Define cómo se asegura que el producto cumple los criterios de éxito y los requerimientos vigentes: criterios de aceptación, métricas, actividades de aseguramiento por hito, niveles de prueba, gestión de defectos, gestión de configuración y compuertas de calidad. Cada prueba referencia el requerimiento que verifica, para mantener la trazabilidad completa.

## **1. Criterios de aceptación del proyecto**

*Acta — Criterios de éxito.*

| ID | Criterio de éxito (Acta; Alcance §6) | Cómo se verifica | Requerimientos | Actividad · Hito |
| :---- | :---- | :---- | :---- | :---- |
| CE-1 | El sistema emite facturas electrónicas válidas contra el ambiente de homologación de ARCA (CAE obtenido correctamente). | Prueba de integración contra homologación: Factura A, B y C, Nota de Crédito y Nota de Débito; evidencia del CAE devuelto y del log sin credenciales. | RF-06, RF-08, RF-09 | 4.2, 4.3, 4.7, 9.3 · H2/H4 |
| CE-2 | El sistema permite operar el ciclo completo: alta de producto → venta con control de stock → facturación → registro de pago → impacto en reportes. | Prueba de sistema de extremo a extremo con datos de ejemplo; conciliación entre venta, comprobante, pago y reporte. | RF-31 | 9.1 · H4 |
| CE-3 | El modelo de datos es aplicable a al menos 2 rubros distintos (kiosco e indumentaria) sin cambios de código, solo de configuración/datos. | Demostración: configurar dos rubros con categorías y variantes propias y repetir CE-2 sin modificar el código; revisión del repositorio. | RF-32, RNF-01 a RNF-03 | 2.4, 9.2 · H1/H4 |

## **2. Objetivos y métricas de calidad**

*Meta propuesta · origen trazable.*

| Métrica | Meta propuesta | Cómo se mide | Origen | Frecuencia |
| :---- | :---- | :---- | :---- | :---- |
| Requerimientos de prioridad Alta con prueba aprobada | 100% al cierre de H4 | Matriz de trazabilidad (§5) | Requerimientos | Cierre de hito |
| Casos de facturación con CAE en homologación | 100% de los tipos (A, B, C, NC, ND) | Registro de pruebas de 4.2, 4.3, 4.7 y 9.3 | RF-06, RF-07, CE-1 | H2 y H4 |
| Defectos críticos abiertos | 0 al cierre de cada hito | Registro de defectos | Este plan (§6) | Semanal |
| Secretos (certificados, claves, CUIT reales) en el repositorio | 0 | Escaneo de secretos antes de cada integración | RNF-04 | Cada integración |
| Secretos en logs de la aplicación | 0 | Revisión de logs en pruebas de 4.4 y 4.7 | RNF-05, RF-10 | H2 y H4 |
| Rubros validados sin cambio de código | ≥ 2 rubros, 0 líneas modificadas | Prueba 9.2 | RF-32, CE-3 | H4 |
| IVA y tipos de comprobante parametrizables | Cambio solo por configuración | Prueba de configuración | RNF-03 | H2 |
| Interfaz responsive | Uso correcto en ≥ 2 anchos de pantalla (escritorio y móvil) | Inspección en navegador | RNF-06 | H3 y H4 |
| Retrabajo (defectos reabiertos / defectos cerrados) | < 10% | Registro de defectos | Meta propuesta del equipo | Cierre de hito |

*Las metas son propuestas del equipo, basadas en los criterios de éxito y requerimientos no funcionales ya definidos; se validan con el Sponsor en la revisión de H1 y se ajustan por control de cambios.*

## **3. Actividades de aseguramiento por hito**

| Hito | Actividades de aseguramiento de calidad | Actividad de la Lista | Responsable |
| :---- | :---- | :---- | :---- |
| H1 | Revisión de pares de Acta, Interesados, Requerimientos, Alcance, EDT y Lista de Actividades (consistencia y trazabilidad); revisión del modelo de datos contra dos rubros de ejemplo; criterios de aceptación de CE-1 a CE-3 acordados. | 1.5, 2.4 | Jesus (revisión) · Tomás |
| H2 | Pruebas unitarias de cada módulo; pruebas de integración contra homologación (WSAA/WSFEv1); revisión de logs y repositorio por secretos; pruebas funcionales y regresión del módulo Productos y Stock. | 3.5, 4.7 | Jesus · Tomás · Juan |
| H3 | Pruebas funcionales de Clientes/Proveedores, Pagos/Giftcards, Reportes y Roles; pruebas de pasarela simulada; prueba de permisos por rol; regresión de H2. | 5.4, 6.5, 7.7, 8.3 | Jesus · Juan · Tomás |
| H4 | Ciclo integral (CE-2); genericidad en 2 rubros (CE-3); validación final de homologación (CE-1); regresión completa; aceptación con el Sponsor y un comerciante representativo. | 9.1, 9.2, 9.3, 9.4 | Jesus |

## **4. Estrategia de pruebas**

*Niveles de prueba.*

| Nivel | Alcance de la prueba | Responsable | Entorno / datos |
| :---- | :---- | :---- | :---- |
| Unitaria | Lógica de negocio de cada módulo (cálculo de stock, saldos, giftcards, impuestos). | Autor del código | Local, datos de ejemplo |
| Integración | Módulos entre sí y cliente de los WS de ARCA (homologación); manejo de errores sin asumir CAE. | Tomás con Jesus | Homologación de ARCA con CUIT de prueba |
| Sistema / E2E | Flujos completos de la aplicación, incluido el ciclo integral y los roles. | Jesus | Servidor Railway (entorno de pruebas) |
| Seguridad | Ausencia de secretos en repositorio y logs; acceso por rol. | Jesus | Repositorio y logs |
| Aceptación | Verificación de los criterios de éxito CE-1 a CE-3 con el Sponsor. | Sponsor y Director | Entorno de pruebas; dos rubros configurados |

En H2 y H3 el trabajo se organiza en los sprints S1–S8 (Cronograma §2). Los defectos abiertos forman parte del backlog del sprint siguiente: cada revisión de sprint informa al equipo los defectos críticos y mayores abiertos, que se priorizan antes de nuevas funcionalidades (§6). Las pruebas funcionales de cada módulo (3.5, 4.7, 5.4, 6.5, 7.7 y 8.3) se ejecutan al cierre del hito, no al cierre de cada sprint.

*Hasta que se implemente el rol administrador (8.1) los módulos operan con un usuario único provisorio de perfil administrador; las pruebas de permisos se concentran en 8.3 (PC-USR).*

## **5. Matriz de trazabilidad requerimiento → prueba**

*Cobertura RF/RNF.*

| ID prueba | Requerimientos | Verificación | EDT | Actividad que la ejecuta | Hito |
| :---- | :---- | :---- | :---- | :---- | :---- |
| PC-STK | RF-01 a RF-05 | Pruebas funcionales: CRUD, categorías y variantes configurables, ajuste con motivo y alerta de stock mínimo | 3.1–3.5 | 3.5 | H2 |
| PC-ARCA | RF-06 a RF-11; RNF-04, 05, 09 | Integración en homologación: A/B/C, NC/ND; error simulado de WS; logs sin credenciales; PDF | 4.1–4.7 | 4.7 | H2 |
| PC-CLI | RF-12 a RF-14 | Funcionales: ABM con datos fiscales; saldo, movimientos y límite de crédito; estado de cuenta | 5.1–5.4 | 5.4 | H3 |
| PC-PAG | RF-15 a RF-21 | Funcionales: cinco medios de pago, pago mixto, ciclo de giftcards y pasarela simulada | 6.1–6.5 | 6.5 | H3 |
| PC-REP | RF-22 a RF-27 | Funcionales: cinco reportes y exportación; conciliación con ventas | 7.1–7.7 | 7.7 | H3 |
| PC-USR | RF-28 a RF-30 | Pruebas de permisos: administrador vs. cajero | 8.1–8.3 | 8.3 | H3 |
| PC-E2E | RF-31 (CE-2) | Sistema: alta → venta → facturación → pago → reportes | 9.1 | 9.1 | H4 |
| PC-GEN | RF-32; RNF-01 a RNF-03 (CE-3) | Demostración con dos rubros sin cambio de código | 2.2, 2.4, 9.2 | 2.4, 9.2 | H1/H4 |
| PC-HOM | CE-1; RF-06, 08, 09 | Validación final contra homologación | 9.3 | 9.3 | H4 |
| PC-NF | RNF-06, 07, 08, 10 | Inspección de interfaz responsive; verificación de que lo excluido no se implementó, de que los cambios pasaron por el proceso de control y de que el equipo se mantuvo fijo (registro de horas por integrante) | 9.1, 9.4 | 9.1, 9.4 | H3/H4 |

*Todos los RF (RF-01 a RF-32) y todos los RNF (RNF-01 a RNF-10) tienen al menos una prueba asignada.*

## **6. Gestión de defectos**

*Severidad y flujo.*

| Severidad | Criterio | Tratamiento |
| :---- | :---- | :---- |
| Crítico | Impide emitir comprobantes o completar el ciclo integral; expone credenciales o corrompe saldos/stock. | Se corrige antes de continuar con funcionalidades nuevas; bloquea el cierre del hito. |
| Mayor | Una funcionalidad incluida no opera como se requiere y no hay alternativa razonable. | Se corrige antes del cierre del hito o se acuerda un plan con el Director. |
| Menor | Funcionalidad con alternativa o comportamiento no deseado de bajo efecto. | Se prioriza en el backlog del hito siguiente. |
| Cosmético | Aspecto visual o texto sin efecto funcional. | Se corrige si hay capacidad. |

Flujo del defecto: registrar → clasificar → asignar → corregir → verificar → cerrar. Todo defecto se registra con el requerimiento afectado, pasos para reproducirlo y responsable; el cierre exige evidencia de la reprueba y regresión del área.

## **7. Criterios de entrada y salida por hito (compuertas)**

*Quality gates.*

| Hito | Criterio de entrada | Criterio de salida (compuerta) |
| :---- | :---- | :---- |
| H1 | Acta emitida (19/08/2026) y aprobada por el Sponsor. | Documentos de gestión aprobados (revisión de pares 1.5 cerrada); stack y modelo de datos definidos; modelo revisado contra dos rubros (2.4); spike con conexión a homologación documentada y un CAE de homologación obtenido para una factura de prueba; criterios CE-1 a CE-3 acordados. |
| H2 | H1 aprobado; CUIT de prueba y certificado de testing disponibles (R4 confirmado el 07/10/2026). | PC-STK y PC-ARCA aprobadas; CAE obtenido en homologación para A/B/C y NC/ND; 0 críticos abiertos; 0 secretos en repositorio y logs. |
| H3 | H2 aprobado; mecanismo de ambiente homologación/producción configurable (4.6; no requiere credenciales reales). | PC-CLI, PC-PAG, PC-REP y PC-USR aprobadas; regresión de H2 sin fallas; 0 críticos abiertos. |
| H4 | H3 aprobado; funcionalidad completa. | PC-E2E, PC-GEN y PC-HOM aprobadas (CE-1 a CE-3 cumplidos); regresión completa; 0 críticos y plan para los mayores; documentación de cierre entregada. |

*Estado al 07/10/2026 (semana 8): H1 no tiene acta de revisión de hito ni evidencia en `docs/` de 1.5 y 2.1–2.4. La entrada de H2 relativa a la CUIT de prueba y al certificado de testing quedó confirmada (riesgo R4). H2 está en ejecución sin cumplir la salida de H1: hasta documentar el cierre de H1 (o aprobar el desvío por control de cambios), esa condición se registra como incumplida (Plan de Proyecto §5, observación 9).*

## **8. Gestión de configuración y versiones**

*Plan de cambios / configuración.*

| Elemento | Norma |
| :---- | :---- |
| Repositorio de código | Un repositorio único con rama principal estable por hito, rama de integración y ramas de trabajo por funcionalidad; etiqueta (tag) al cerrar H1, H2, H3 y H4. Commits con el formato `[frontend\|backend\|qa\|docs] descripción breve`. |
| Secretos | Certificados (.crt/.key), CUIT reales y credenciales de producción nunca se versionan: variables de entorno o archivos ignorados por git (RNF-04). |
| Ambientes | Desarrollo local contra homologación de ARCA (por defecto, RNF-09); servidor Railway para pruebas; credenciales de producción solo para la validación final opcional. |
| Documentos | Se versionan en el repositorio (carpeta `docs/`), cada uno con tabla de versiones; todo cambio aprobado por el proceso de control de cambios (Alcance §7) incrementa la versión del documento afectado y del Documento de Requerimientos. |
| Cambios de alcance | Registro → análisis de impacto → decisión (Director o Sponsor) → actualización de documentos → comunicación (Alcance §7). |
