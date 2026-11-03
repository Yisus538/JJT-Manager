JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Presupuesto y Estimación al Cierre — Estado a la Semana 12**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-20 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Elaboró | Jesus Manuel Martinez (QA y QC) |
| Corte | 03/11/2026 (semana 12) |
| Fecha / Versión / Estado | 03/11/2026 · 1.0 · Borrador: avance declarado por el equipo; costo real pendiente de registro |

> Actualiza la lectura de costos de la Estimación y Presupuesto (JJT-GPI-08 v1.2) con el avance declarado al 03/11/2026. Tomando el presupuesto, las horas y la tarifa de JJT-GPI-08 sin cambios, calcula el valor ganado, el trabajo restante y los escenarios de cierre. **El costo real (AC) no está registrado en el repositorio**, de modo que el CPI no puede calcularse todavía: este documento deja la fórmula y los escenarios en su lugar, sin inventar el dato.

## **1. Presupuesto base (sin cambios)**

| Concepto | Horas | USD |
| :---- | :----: | :----: |
| Esfuerzo esperado, BAC (48 actividades, USD 25/h) | 970 | 24.250 |
| Reserva (contingencia y gestión) | 110 | 2.750 |
| **Personal total (techo del Acta)** | **1.080** | **27.000** |
| Infraestructura (Railway, USD 5/mes × 5 meses) | — | 25 |
| **Presupuesto total** | | **27.025** |

Rango de esfuerzo de la estimación de tres puntos: 760 a 1.220 h; tarifa única de USD 25/h para los tres integrantes.

## **2. Avance al 03/11/2026 (valor ganado)**

Actividades que el cronograma prevé terminadas al 01/11/2026 y que el equipo declara realizadas (1.1–1.5, 2.1–2.4, 3.1–3.4 y 4.1.1–4.2):

| Paquete | Actividades | Horas | USD |
| :---- | :---- | :----: | :----: |
| 1.0 Gestión | 1.1 a 1.5 | 60 | 1.500 |
| 2.0 Diseño | 2.1 a 2.4 | 100 | 2.500 |
| 3.0 Productos y Stock | 3.1 a 3.4 | 95 | 2.375 |
| 4.0 Facturación | 4.1.1, 4.1.2, 4.1.3 y 4.2 | 82 | 2.050 |
| **Valor ganado (EV)** | 17 de 48 actividades | **337** | **8.425** |

| Indicador | Valor | Cómo se calcula |
| :---- | :----: | :---- |
| EV (valor ganado) | USD 8.425 | 337 h × USD 25; 34,7% del BAC |
| PV (valor planificado al cierre de la sem. 11) | USD 8.725 (349 h) | Suma de la carga semanal del Cronograma §6, sem. 1 a 11 |
| SV (variación de plazo) | −USD 300 (−12 h) | EV − PV |
| SPI | 0,97 | EV / PV |
| AC (costo real) | **Sin dato** | Requiere el registro de horas por integrante |
| CPI | **Sin dato** | EV / AC |

La diferencia de 12 h con el plan corresponde a la mitad de 4.3 (Notas de Crédito/Débito, sem. 11–12), que está en curso y no se acredita hasta cerrarla. Si el equipo la termina esta semana, el SPI vuelve a 1,0.

## **3. Trabajo restante (ETC) y capacidad**

| Integrante | Horas del plan | Realizadas (EV) | Restantes | Capacidad sem. 12–27 (16 sem. × 13,3 h) | Diferencia |
| :---- | :----: | :----: | :----: | :----: | :----: |
| Tomás (Backend/PM) | 323 | 197 | 126 | 213 | +87 |
| Juan (Frontend) | 324 | 95 | 229 | 213 | −16 |
| Jesus (QA/QC) | 323 | 45 | 278 | 213 | **−65** |
| **Total** | 970 | 337 | 633 | 640 | +7 |

- Restante del plan: 633 h, USD 15.825; con la reserva completa, 743 h y USD 18.575 (el saldo del techo de USD 27.000).
- La capacidad total alcanza (640 h contra 633 h), pero está mal repartida en el tiempo: Jesus concentra 278 h hacia H3 y H4 y supera su capacidad en 65 h; Tomás tendrá 87 h libres cuando termine Facturación y Clientes. **Propuesta para el Director:** que Tomás tome horas de apoyo en las pruebas de integración ARCA (4.7) y en 9.3, y que la reasignación pase por control de cambios, porque modifica el reparto de JJT-GPI-08 §4.
- Pendiente no financiado: la gestión continua (informes, registro de horas, SPI/CPI, revisiones de sprint) sigue sin horas asignadas (observación 17 del Plan de Proyecto) y se cubre con la reserva.

## **4. Pronóstico al cierre (EAC)**

Como el CPI no está medido, se muestran escenarios con la fórmula EAC = BAC / CPI:

| CPI supuesto | EAC (h) | EAC (USD, personal) | Frente al techo de USD 27.000 |
| :----: | :----: | :----: | :---- |
| 1,10 | 882 | 22.045 | Margen de USD 4.955 |
| 1,00 | 970 | 24.250 | Margen de USD 2.750 (la reserva íntegra) |
| 0,90 | 1.078 | 26.944 | Margen de USD 56: sin reserva |
| 0,85 | 1.141 | 28.529 | Excede el techo en USD 1.529 |
| 0,80 | 1.213 | 30.313 | Excede el techo en USD 3.313 |

**CPI mínimo tolerable: 0,90** (BAC ÷ techo de personal). Por debajo de ese valor, el costo supera el presupuesto aprobado y corresponde un pedido de aprobación al Sponsor (Alcance §7). El nivel de alerta del Plan de Comunicaciones (50% de la reserva consumida, USD 1.375) se evalúa apenas haya horas reales.

## **5. Infraestructura**

Railway: USD 5 por mes desde octubre de 2026. Si el servidor se contrató al inicio de H2, el gasto a la fecha es de USD 10 y quedan USD 15. El equipo debe confirmar la fecha de contratación y el importe real.

## **6. Datos que faltan para cerrar este documento**

| Dato | Responsable | Para qué |
| :---- | :---- | :---- |
| Horas reales por integrante y por actividad, de la semana 1 a la 12 | Tomás, Juan y Jesus | Calcular AC y CPI y pasar el EAC de escenario a pronóstico |
| Fecha y monto de contratación de Railway | Tomás | Costo real de infraestructura |
| Confirmación de 4.3 (cerrada o en curso) | Tomás | Ajustar EV y SPI |
| Decisión sobre reasignación de horas de QA | Tomás | Corregir el desbalance de Jesus |
