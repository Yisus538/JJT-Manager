JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Estimación de Esfuerzo y Presupuesto**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-08 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Horizonte | 27 semanas (19/08/2026 – 21/02/2027; semanas contadas desde el lunes 17/08/2026) |
| Fecha / Versión / Estado | 07/10/2026 · 1.2 · Aprobado por el Sponsor |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 05/10/2026 | Emisión inicial (borrador). |
| 1.1 | 06/10/2026 | Pasa a formato Markdown. Se reparten las horas entre las 48 actividades de la Lista v1.1 (se incorporan las 8 actividades de QA por módulo con las horas de Jesus que antes no estaban asignadas a ninguna actividad). Se eliminan citas bibliográficas internas. Se agrega la sensibilidad de la estimación con la fórmula PERT y se aclara que la reserva queda comprometida (ver Plan de Riesgos §4). Totales por paquete, por rol, por hito y presupuesto: sin cambios. |
| 1.2 | 07/10/2026 | La tabla de §4 se hace coherente con las horas por actividad de §3 (la versión anterior no lo era: Jesus figuraba con 83 h de 9.0 aunque las cuatro actividades de 9.x eran suyas, lo que sumaba 370 h para Jesus, 335 para Tomás y 265 para Juan). Se redistribuyen 63 h de apoyo entre integrantes según su rol y la carga queda en 323/324/323 h. Se declara que la gestión continua y los documentos 07–12 no tienen horas asignadas (§7), en lugar de afirmar que están incluidas en 1.0. |

> Estimación de esfuerzo y presupuesto. Desarrolla la estimación del proyecto en horas y costos a partir de la EDT y de la Lista de Actividades, respetando el presupuesto de alto nivel del Acta v1.2 (1.080 h de personal = USD 27.000, más USD 25 de infraestructura = USD 27.025). La estimación es una aproximación explícita, reproducible y revisable: se comunica como rango con sus supuestos, no como una promesa.

**970 h** esfuerzo esperado (rango 760–1.220 h) · **1.080 h** presupuesto de horas (Acta) · **110 h** reserva (11,3% sobre lo esperado) · **USD 27.025** presupuesto total (personal + infraestructura)

## **1. Estimación, objetivo y compromiso**

| Concepto | Pregunta | Valor en JJT Manager | Origen |
| :---- | :---- | :---- | :---- |
| Estimación | ¿Qué creemos que ocurrirá? | 970 h esperadas (rango 760–1.220 h) | Este documento, §2 |
| Objetivo / presupuesto | ¿Cuánto asignamos? | 1.080 h = USD 27.000 (3 integrantes × USD 25/h) + USD 25 de infraestructura | Acta — Presupuesto de alto nivel |
| Compromiso | ¿Qué acordamos? | Hitos H1–H4 y fin estimado 21/02/2027 (27 semanas) | Acta — Hitos; Alcance §3 |

Se mantienen separados los tres conceptos para no convertir una estimación incierta en una promesa artificialmente precisa. La diferencia entre el presupuesto y la estimación esperada (110 h, 11,3%) constituye la reserva del proyecto.

## **2. Estimación por paquete de trabajo (tres puntos)**

*EDT 1.0–9.0.*

Cada paquete de la EDT se estimó con juicio de experto del equipo y tres puntos (optimista O, más probable M, pesimista P), usando el promedio simple de los tres puntos: E = (O + M + P) / 3. Las horas esperadas por paquete coinciden con la suma de las horas de sus actividades (§3).

| EDT | Paquete de trabajo | O (h) | M (h) | P (h) | E (h) | % total | Resp. | Hito |
| :---- | :---- | :----: | :----: | :----: | :----: | :----: | :---- | :---- |
| 1.0 | Gestión del Proyecto | 50 | 60 | 70 | 60 | 6,2% | Tomás | H1 |
| 2.0 | Diseño y Arquitectura | 80 | 100 | 120 | 100 | 10,3% | Tomás | H1 |
| 3.0 | Módulo Productos y Stock | 100 | 120 | 155 | 125 | 12,9% | Juan | H2 |
| 4.0 | Módulo Facturación (ARCA) | 190 | 230 | 300 | 240 | 24,7% | Tomás | H2 |
| 5.0 | Clientes/Proveedores y Cuentas Corrientes | 60 | 75 | 105 | 80 | 8,2% | Tomás | H3 |
| 6.0 | Módulo Pagos y Giftcards | 80 | 100 | 135 | 105 | 10,8% | Juan | H3 |
| 7.0 | Módulo Reportes y Estadísticas | 70 | 85 | 115 | 90 | 9,3% | Juan | H3 |
| 8.0 | Módulo Usuarios y Permisos | 30 | 40 | 50 | 40 | 4,1% | Juan | H3 |
| 9.0 | Pruebas, Integración y Cierre | 100 | 120 | 170 | 130 | 13,4% | Jesus | H4 |
| | **Total del proyecto** | 760 | 930 | 1220 | 970 | 100% | | |

*Rango de esfuerzo: 760–1,220 h (suma de O y de P; no se interpreta como intervalo de confianza). Estimación esperada: 970 h. Presupuesto de horas del Acta: 1.080 h.*

**Sensibilidad:** con la fórmula PERT (O + 4M + P) / 6 el esperado sería 950 h (−20 h respecto del promedio simple), todavía dentro del presupuesto de 1.080 h. El equipo mantiene el promedio simple (no hay datos históricos propios que justifiquen ponderar el valor más probable); ambas fórmulas dan un resultado inferior al presupuesto.

## **3. Estimación por actividad**

*Lista de Actividades v1.1 · 48 actividades.*

| ID | Actividad | Resp. | Horas | % del paquete | Trazabilidad |
| :---- | :---- | :---- | :----: | :----: | :---- |
| 1.1 | Acta de Constitución | Tomás | 8 | 13% | Acta |
| 1.2 | Registro de Interesados | Tomás | 8 | 13% | Acta |
| 1.3 | Documento de Requerimientos | Tomás | 16 | 27% | Acta |
| 1.4 | Documento de Alcance y Gestión | Tomás | 13 | 22% | Acta |
| 1.5 | Revisión de pares de los documentos de gestión | Jesus | 15 | 25% | Plan de Calidad §3 |
| 2.1 | Definición de stack tecnológico | Tomás | 11 | 11% | RNF-01 a 03 |
| 2.2 | Modelo de datos genérico multirubro | Tomás | 28 | 28% | RNF-01 a 03 |
| 2.3 | Spike técnico homologación ARCA | Tomás | 31 | 31% | Acta (Riesgos) |
| 2.4 | Revisión del modelo de datos contra 2 rubros | Jesus | 30 | 30% | RF-32; RNF-01 a 03 |
| 3.1 | Alta/baja/modificación de productos | Juan | 27 | 22% | RF-01 |
| 3.2 | Categorías y variantes configurables | Juan | 27 | 22% | RF-02, 03 |
| 3.3 | Control de inventario y ajustes | Juan | 26 | 21% | RF-04 |
| 3.4 | Alertas de stock mínimo | Juan | 15 | 12% | RF-05 |
| 3.5 | Pruebas funcionales de Productos y Stock | Jesus | 30 | 24% | RF-01 a 05 |
| 4.1.1 | Autenticación WSAA | Tomás | 17 | 7% | RF-06, 08 |
| 4.1.2 | Cacheo y renovación del ticket | Tomás | 10 | 4% | RF-06, 08 |
| 4.1.3 | Cliente WSFEv1 | Tomás | 21 | 9% | RF-06, 08 |
| 4.2 | Emisión de Factura A/B/C | Tomás | 34 | 14% | RF-06 |
| 4.3 | Notas de Crédito/Débito | Tomás | 24 | 10% | RF-07 |
| 4.4 | Errores de WS y logging seguro | Tomás | 21 | 9% | RF-09, 10; RNF-05 |
| 4.5 | Exportación de comprobantes PDF | Tomás | 17 | 7% | RF-11 |
| 4.6 | Credenciales de producción | Tomás | 21 | 9% | RF-08; RNF-04, 09 |
| 4.7 | Pruebas de integración contra homologación ARCA | Jesus | 75 | 31% | RF-06 a 11; RNF-04, 05, 09 |
| 5.1 | ABM clientes/proveedores | Tomás | 21 | 26% | RF-12 |
| 5.2 | Cuentas corrientes | Tomás | 22 | 28% | RF-13 |
| 5.3 | Consulta de estado de cuenta | Tomás | 12 | 15% | RF-14 |
| 5.4 | Pruebas funcionales de Clientes/Proveedores | Jesus | 25 | 31% | RF-12 a 14 |
| 6.1.1 | Efectivo y cuenta corriente | Juan | 7 | 7% | RF-15 |
| 6.1.2 | Débito/crédito y transferencia | Juan | 9 | 9% | RF-15 |
| 6.1.3 | QR | Juan | 14 | 13% | RF-15, 21 |
| 6.2 | Pago combinado / mixto | Juan | 13 | 12% | RF-16 |
| 6.3 | Giftcards | Juan | 20 | 19% | RF-17 a 20 |
| 6.4 | Pasarela simulada/sandbox | Juan | 12 | 11% | RF-21 |
| 6.5 | Pruebas funcionales de Pagos y Giftcards | Jesus | 30 | 29% | RF-15 a 21 |
| 7.1 | Ventas por período | Juan | 13 | 14% | RF-22 |
| 7.2 | Productos más vendidos | Juan | 9 | 10% | RF-23 |
| 7.3 | Stock crítico | Juan | 7 | 8% | RF-24 |
| 7.4 | Cuentas corrientes | Juan | 9 | 10% | RF-25 |
| 7.5 | Rentabilidad | Juan | 14 | 16% | RF-26 |
| 7.6 | Exportación de reportes | Juan | 13 | 14% | RF-27 |
| 7.7 | Pruebas funcionales de Reportes | Jesus | 25 | 28% | RF-22 a 27 |
| 8.1 | Rol administrador | Juan | 17 | 42% | RF-28, 29 |
| 8.2 | Rol cajero | Juan | 13 | 32% | RF-28, 30 |
| 8.3 | Pruebas de permisos por rol | Jesus | 10 | 25% | RF-28 a 30 |
| 9.1 | Ciclo integral | Jesus | 45 | 35% | RF-31; RNF-06 |
| 9.2 | Genericidad en ≥2 rubros | Jesus | 30 | 23% | RF-32 |
| 9.3 | Validación final ARCA | Jesus | 25 | 19% | Acta (Criterios de éxito) |
| 9.4 | Entrega final y cierre | Jesus | 30 | 23% | Acta; RNF-07, 08, 10 |
| | **Total (48 actividades)** | | **970** | | |

*El reparto por actividad es una distribución del esfuerzo esperado de cada paquete (§2) acordada por el equipo; la columna Trazabilidad usa los RF/RNF indicados en la EDT. En la v1.1 las actividades de QA (1.5, 2.4, 3.5, 4.7, 5.4, 6.5, 7.7, 8.3) llevan exactamente las horas de Jesus de cada paquete según §4; las demás actividades se redistribuyeron proporcionalmente para mantener el total de cada paquete.*

## **4. Recursos y esfuerzo por rol**

*Acta — Equipo.*

Distribución del esfuerzo esperado por integrante según su rol (Acta — Equipo; Alcance — Equipo y responsabilidades). El Acta fija una tarifa única de USD 25/h y el presupuesto de 1.080 h equivale a 360 h por integrante.

| EDT | Paquete de trabajo | Tomás (Backend/PM) | Juan (Frontend) | Jesus (QA/QC) | Total h |
| :---- | :---- | :----: | :----: | :----: | :----: |
| 1.0 | Gestión del Proyecto | 45 | 0 | 15 | 60 |
| 2.0 | Diseño y Arquitectura | 70 | 0 | 30 | 100 |
| 3.0 | Módulo Productos y Stock | 0 | 95 | 30 | 125 |
| 4.0 | Módulo Facturación (ARCA) | 162 | 3 | 75 | 240 |
| 5.0 | Clientes/Proveedores y Cuentas Corrientes | 42 | 13 | 25 | 80 |
| 6.0 | Módulo Pagos y Giftcards | 0 | 75 | 30 | 105 |
| 7.0 | Módulo Reportes y Estadísticas | 0 | 65 | 25 | 90 |
| 8.0 | Módulo Usuarios y Permisos | 0 | 30 | 10 | 40 |
| 9.0 | Pruebas, Integración y Cierre | 4 | 43 | 83 | 130 |
| | **Esfuerzo esperado** | **323** | **324** | **323** | **970** |
| | Reserva (distribución equitativa) | 37 | 36 | 37 | 110 |
| | **Total con reserva (h)** | **360** | **360** | **360** | **1.080** |

Jesus (QA/QC) ejecuta el paquete 9.0 junto con una actividad de QA propia en cada módulo (1.5, 2.4, 3.5, 4.7, 5.4, 6.5, 7.7 y 8.3, que suman 240 h). Tomás y Juan comparten las tareas de pruebas de componente de su propio desarrollo (pruebas unitarias dentro de las horas de cada actividad).

**Horas de apoyo entre integrantes.** Cada actividad conserva un responsable principal (§3, Lista y Cronograma), pero parte de sus horas las ejecuta otro integrante según su rol. Con estas transferencias la carga queda equilibrada (323/324/323 h) y cada integrante tiene 360 h disponibles con la reserva repartida de forma equitativa:

| Actividad | Horas | Responsable principal | Apoyo | Qué hace el apoyo |
| :---- | :----: | :---- | :---- | :---- |
| 4.5 Exportación de comprobantes PDF | 17 | Tomás (14 h) | Juan (3 h) | Diseño y maquetado del comprobante imprimible |
| 5.1 ABM clientes/proveedores | 21 | Tomás (13 h) | Juan (8 h) | Formularios y pantallas de alta, baja y modificación |
| 5.3 Consulta de estado de cuenta | 12 | Tomás (7 h) | Juan (5 h) | Vista de estado de cuenta |
| 9.1 Ciclo integral | 45 | Jesus (26 h) | Juan (19 h) | Ajustes de interfaz y revisión responsive (RNF-06) de los defectos detectados; carga de datos de demostración |
| 9.2 Genericidad en ≥2 rubros | 30 | Jesus (16 h) | Juan (14 h) | Configuración de catálogo, categorías y variantes de los dos rubros |
| 9.3 Validación final ARCA | 25 | Jesus (21 h) | Tomás (4 h) | Soporte de la integración WSAA/WSFEv1 y análisis de rechazos |
| 9.4 Entrega final y cierre | 30 | Jesus (20 h) | Juan (10 h) | Demostración y validación con el comerciante (Plan de Comunicaciones §2) y ajustes de usabilidad |

El reparto de §3 sigue siendo por actividad; los totales por paquete, por hito y el presupuesto no cambian.

## **5. Capacidad frente a demanda por hito**

*40 h/semana.*

La capacidad se calcula como 40 h por semana del equipo (1.080 h ÷ 27 semanas del Acta = 40 h/semana, es decir, aproximadamente 13,3 h por integrante).

| Hito | Semanas | N.º sem. | Capacidad (h) | Demanda esperada (h) | Ocupación | Holgura (h) |
| :---- | :---- | :----: | :----: | :----: | :----: | :----: |
| H1 | 1–6 | 6 | 240 | 160 | 67% | +80 |
| H2 | 7–15 | 9 | 360 | 365 | 101% | −5 |
| H3 | 16–23 | 8 | 320 | 315 | 98% | +5 |
| H4 | 24–27 | 4 | 160 | 130 | 81% | +30 |
| Total | 1–27 | 27 | 1080 | 970 | 90% | +110 |

Lectura: la demanda esperada de H2 (365 h) supera en 5 h la capacidad del hito, mientras que H1 y H4 tienen holgura de 80 h y 30 h. La holgura total (110 h) coincide con la reserva del proyecto, es decir, **la reserva ya cubre el exceso de H2 y no es "libre"**: cada hora de H2 que se consuma de más sale directamente de la reserva. Por eso H2 —que contiene la ruta crítica y el riesgo ARCA— debe monitorearse con mayor frecuencia (ver Plan de Comunicaciones y Seguimiento). La carga semanal detallada y su nivelación están en el Cronograma §6.

## **6. Costos y presupuesto**

*Acta — Presupuesto de alto nivel.*

| EDT | Concepto | Horas | Costo (USD 25/h) |
| :---- | :---- | :----: | :----: |
| 1.0 | Gestión del Proyecto | 60 | $1.500 |
| 2.0 | Diseño y Arquitectura | 100 | $2.500 |
| 3.0 | Módulo Productos y Stock | 125 | $3.125 |
| 4.0 | Módulo Facturación (ARCA) | 240 | $6.000 |
| 5.0 | Clientes/Proveedores y Cuentas Corrientes | 80 | $2.000 |
| 6.0 | Módulo Pagos y Giftcards | 105 | $2.625 |
| 7.0 | Módulo Reportes y Estadísticas | 90 | $2.250 |
| 8.0 | Módulo Usuarios y Permisos | 40 | $1.000 |
| 9.0 | Pruebas, Integración y Cierre | 130 | $3.250 |
| | **Subtotal esfuerzo esperado** | **970** | **$24.250** |
| | Reserva (contingencia y gestión) | 110 | $2.750 |
| | **Costo de personal total (coincide con el Acta)** | **1.080** | **$27.000** |

| Costo | Detalle | Importe |
| :---- | :---- | :----: |
| Infraestructura | Railway (servidor): USD 5/mes × 5 meses (oct/2026–feb/2027; se asume contratación al inicio de H2, semana 7, con primer cobro en octubre) | $25 |
| Personal | 1.080 h × USD 25/h (Acta — Presupuesto de alto nivel) | $27.000 |
| **Presupuesto total estimado** | | **$27.025** |

Línea base de costo por hito (valor planificado acumulado, sin reserva). Es la referencia contra la que se mide el avance en el Plan de Comunicaciones y Seguimiento (JJT-GPI-11, §5).

| Hito | Horas del hito | Costo del hito | Horas acum. | PV acumulado | % de la línea base |
| :---- | :----: | :----: | :----: | :----: | :----: |
| H1 | 160 | $4.000 | 160 | $4.000 | 16% |
| H2 | 365 | $9.125 | 525 | $13.125 | 54% |
| H3 | 315 | $7.875 | 840 | $21.000 | 87% |
| H4 | 130 | $3.250 | 970 | $24.250 | 100% |
| **BAC** | **970** | **$24.250** | **970** | **$24.250** | **100%** |

*BAC (presupuesto hasta la finalización, sin reserva) = USD 24.250. La reserva de 110 h (USD 2.750) se gestiona fuera de la línea base y solo se libera mediante decisión del Director de Proyecto (reserva de contingencia, ver Plan de Riesgos, §5) o aprobación del Sponsor (reserva de gestión).*

## **7. Supuestos, restricciones y calibración**

- Estimación basada en el alcance vigente (Documento de Alcance, §1); un cambio de alcance obliga a re-estimar (Alcance, §7).
- No existen datos históricos de proyectos anteriores del equipo; las estimaciones se apoyan en juicio de experto. Al cierre de cada hito se registra tamaño y esfuerzo real para calibrar (error relativo = |real − estimado| / real).
- La tarifa de USD 25/h es única para los tres integrantes (Acta). Los costos de infraestructura se limitan al servidor Railway.
- La mayor incertidumbre está en 4.0 Facturación (ARCA): su rango (190–300 h) es el más amplio en términos absolutos, lo que se recoge como riesgo R1 del Plan de Riesgos.
- Las 60 h de 1.0 están consumidas por 1.1–1.5 (8 + 8 + 16 + 13 + 15). **No hay horas asignadas** a la gestión continua (reunión de coordinación semanal, informes de estado quincenales o semanales en H2, registro de horas, cálculo de SPI/CPI y revisiones de sprint) ni a la elaboración y mantenimiento de los documentos 07–12. Hasta que el Director de Proyecto decida cómo financiarlas (por ejemplo, una actividad nueva de gestión continua en 1.0, que obliga a re-estimar), se cubren con la reserva, que ya está comprometida (Plan de Riesgos §4): es una exposición adicional no cuantificada.
