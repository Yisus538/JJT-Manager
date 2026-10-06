JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Cronograma del Proyecto**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-07 |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Horizonte | 27 semanas (19/08/2026 – 21/02/2027) |
| Fecha / Versión / Estado | 06/10/2026 · 1.1 · Borrador para revisión |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 05/10/2026 | Emisión inicial (borrador). |
| 1.1 | 06/10/2026 | Pasa a formato Markdown. Incorpora las 48 actividades de la Lista v1.1 (8 de QA por módulo), las dependencias corregidas del paquete 6.0, el calendario de sprints y la carga semanal nivelada (pico 47,8 h en la semana 13, antes 83 h). Se corrige la nomenclatura de la semana 1 y se alinea la ruta crítica con el CPM recalculado. |

> Cronograma base del proyecto. Consolida en un único documento las fechas calendario de los hitos H1–H4, de las 48 actividades de la Lista de Actividades v1.1, los sprints, el diagrama de Gantt, el análisis de ruta crítica y las compuertas de hito. No modifica los hitos del Acta ni los paquetes de trabajo: cualquier ajuste posterior queda sujeto al proceso de control de cambios (Documento de Alcance, §7).

## **1. Calendario e hitos**

*Origen: Acta (Hitos); Alcance §3.*

| Hito | Descripción | Semanas | Inicio | Fin | EDT |
| :---- | :---- | :---- | :---- | :---- | :---- |
| H1 | Planificación, arquitectura y diseño | Sem. 1–6 | 19/08/2026 | 27/09/2026 | 1.0, 2.0 |
| H2 | Desarrollo del sistema central (Stock y Facturación ARCA) | Sem. 7–15 | 28/09/2026 | 29/11/2026 | 3.0, 4.0 |
| H3 | Módulos complementarios (Clientes, Pagos, Reportes y Usuarios) | Sem. 16–23 | 30/11/2026 | 24/01/2027 | 5.0, 6.0, 7.0, 8.0 |
| H4 | Pruebas, integración y entrega final | Sem. 24–27 | 25/01/2027 | 21/02/2027 | 9.0 |

**Convención de calendario:** la semana 1 corresponde a la semana calendario que comienza el lunes 17/08/2026 (el proyecto inicia el miércoles 19/08/2026); cada semana va de lunes a domingo. La semana 27 finaliza el domingo 21/02/2027, fecha estimada de fin del Acta. El Gantt y todos los documentos usan esta misma convención.

## **2. Sprints**

Metodología híbrida (Acta §1; Alcance §3.1): H1 y H4 son fases predictivas; H2 y H3 se ejecutan en sprints de 2 semanas. El último sprint de H2 dura 3 semanas para cerrar junto con el hito. Cada sprint termina con revisión interna y demostración al equipo; el Director de Proyecto prioriza el backlog del sprint junto con el equipo.

| Sprint | Hito | Semanas | Inicio | Fin |
| :---- | :---- | :---- | :---- | :---- |
| S1 | H2 | 7–8 | 28/09/2026 | 11/10/2026 |
| S2 | H2 | 9–10 | 12/10/2026 | 25/10/2026 |
| S3 | H2 | 11–12 | 26/10/2026 | 08/11/2026 |
| S4 | H2 | 13–15 | 09/11/2026 | 29/11/2026 |
| S5 | H3 | 16–17 | 30/11/2026 | 13/12/2026 |
| S6 | H3 | 18–19 | 14/12/2026 | 27/12/2026 |
| S7 | H3 | 20–21 | 28/12/2026 | 10/01/2027 |
| S8 | H3 | 22–23 | 11/01/2027 | 24/01/2027 |

## **3. Cronograma de actividades**

*48 actividades · 9 paquetes de la EDT.*

| ID | Actividad | Resp. | Sem. | Inicio | Fin | Predecesoras |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1.1 | Acta de Constitución | Tomás | 1 | 19/08/2026 | 23/08/2026 | — |
| 1.2 | Registro de Interesados | Tomás | 1 | 19/08/2026 | 23/08/2026 | — |
| 1.3 | Documento de Requerimientos | Tomás | 2 | 24/08/2026 | 30/08/2026 | 1.1, 1.2 |
| 1.4 | Documento de Alcance y Gestión | Tomás | 2 | 24/08/2026 | 30/08/2026 | 1.3 |
| 1.5 | Revisión de pares de los documentos de gestión | Jesus | 2–5 | 24/08/2026 | 20/09/2026 | 1.4 |
| 2.1 | Definición de stack tecnológico | Tomás | 3 | 31/08/2026 | 06/09/2026 | 1.4 |
| 2.2 | Modelo de datos genérico multirubro | Tomás | 3–4 | 31/08/2026 | 13/09/2026 | 2.1 |
| 2.3 | Spike técnico homologación ARCA | Tomás | 4–6 | 07/09/2026 | 27/09/2026 | 2.1 |
| 2.4 | Revisión del modelo de datos contra 2 rubros | Jesus | 4–6 | 07/09/2026 | 27/09/2026 | 2.2 |
| 3.1 | Alta/baja/modificación de productos | Juan | 7–8 | 28/09/2026 | 11/10/2026 | 2.2, 2.3 |
| 3.2 | Categorías y variantes configurables | Juan | 10–11 | 19/10/2026 | 01/11/2026 | 3.1 |
| 3.3 | Control de inventario y ajustes | Juan | 8–9 | 05/10/2026 | 18/10/2026 | 3.1 |
| 3.4 | Alertas de stock mínimo | Juan | 9–10 | 12/10/2026 | 25/10/2026 | 3.3 |
| 3.5 | Pruebas funcionales de Productos y Stock | Jesus | 13–15 | 09/11/2026 | 29/11/2026 | 3.4, 3.2 |
| 4.1.1 | Autenticación WSAA | Tomás | 7 | 28/09/2026 | 04/10/2026 | 2.2, 2.3 |
| 4.1.2 | Cacheo y renovación del ticket | Tomás | 7–8 | 28/09/2026 | 11/10/2026 | 4.1.1 |
| 4.1.3 | Cliente WSFEv1 | Tomás | 8–9 | 05/10/2026 | 18/10/2026 | 4.1.2 |
| 4.2 | Emisión de Factura A/B/C | Tomás | 9–11 | 12/10/2026 | 01/11/2026 | 4.1.3 |
| 4.3 | Notas de Crédito/Débito | Tomás | 11–12 | 26/10/2026 | 08/11/2026 | 4.2 |
| 4.4 | Errores de WS y logging seguro | Tomás | 12–13 | 02/11/2026 | 15/11/2026 | 4.3 |
| 4.5 | Exportación de comprobantes PDF | Tomás | 13–14 | 09/11/2026 | 22/11/2026 | 4.2 |
| 4.6 | Credenciales de producción | Tomás | 14–15 | 16/11/2026 | 29/11/2026 | 4.4 |
| 4.7 | Pruebas de integración contra homologación ARCA | Jesus | 12–15 | 02/11/2026 | 29/11/2026 | 4.3 |
| 5.1 | ABM clientes/proveedores | Tomás | 16–17 | 30/11/2026 | 13/12/2026 | 4.6 |
| 5.2 | Cuentas corrientes | Tomás | 17–18 | 07/12/2026 | 20/12/2026 | 5.1 |
| 5.3 | Consulta de estado de cuenta | Tomás | 18–19 | 14/12/2026 | 27/12/2026 | 5.2 |
| 5.4 | Pruebas funcionales de Clientes/Proveedores | Jesus | 19–21 | 21/12/2026 | 10/01/2027 | 5.3 |
| 6.1.1 | Efectivo y cuenta corriente | Juan | 18 | 14/12/2026 | 20/12/2026 | 5.2, 6.1.3 |
| 6.1.2 | Débito/crédito y transferencia | Juan | 16 | 30/11/2026 | 06/12/2026 | 4.6 |
| 6.1.3 | QR | Juan | 17 | 07/12/2026 | 13/12/2026 | 6.4 |
| 6.2 | Pago combinado / mixto | Juan | 18 | 14/12/2026 | 20/12/2026 | 6.1.1 |
| 6.3 | Giftcards | Juan | 18–19 | 14/12/2026 | 27/12/2026 | 6.2 |
| 6.4 | Pasarela simulada/sandbox | Juan | 16–17 | 30/11/2026 | 13/12/2026 | 6.1.2 |
| 6.5 | Pruebas funcionales de Pagos y Giftcards | Jesus | 19–21 | 21/12/2026 | 10/01/2027 | 6.3 |
| 7.1 | Ventas por período | Juan | 19–20 | 21/12/2026 | 03/01/2027 | 5.3, 6.3 |
| 7.2 | Productos más vendidos | Juan | 20 | 28/12/2026 | 03/01/2027 | 7.1 |
| 7.3 | Stock crítico | Juan | 20–21 | 28/12/2026 | 10/01/2027 | 7.2 |
| 7.4 | Cuentas corrientes | Juan | 21 | 04/01/2027 | 10/01/2027 | 7.3 |
| 7.5 | Rentabilidad | Juan | 21–22 | 04/01/2027 | 17/01/2027 | 7.4 |
| 7.6 | Exportación de reportes | Juan | 22 | 11/01/2027 | 17/01/2027 | 7.5 |
| 7.7 | Pruebas funcionales de Reportes | Jesus | 22–23 | 11/01/2027 | 24/01/2027 | 7.6 |
| 8.1 | Rol administrador | Juan | 22–23 | 11/01/2027 | 24/01/2027 | 7.6 |
| 8.2 | Rol cajero | Juan | 23 | 18/01/2027 | 24/01/2027 | 8.1 |
| 8.3 | Pruebas de permisos por rol | Jesus | 23 | 18/01/2027 | 24/01/2027 | 8.2 |
| 9.1 | Ciclo integral | Jesus | 24–25 | 25/01/2027 | 07/02/2027 | 8.2, 8.3, 7.7, 6.5 |
| 9.2 | Genericidad en ≥2 rubros | Jesus | 25–26 | 01/02/2027 | 14/02/2027 | 9.1 |
| 9.3 | Validación final ARCA | Jesus | 26 | 08/02/2027 | 14/02/2027 | 9.2 |
| 9.4 | Entrega final y cierre | Jesus | 27 | 15/02/2027 | 21/02/2027 | 9.3 |

*Fuente: Lista de Actividades v1.1 (JJT-GPI-06). Resp. = responsable de la actividad (en las actividades de QA, Jesus; en el resto, el responsable del paquete de la EDT).*

## **4. Diagrama de Gantt**

*Semanas 1–27. ■ = actividad de la ruta crítica lógica · □ = actividad con holgura. H1: sem. 1–6 · H2: 7–15 · H3: 16–23 · H4: 24–27.*

| Actividad | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 |
| :---- | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| **1.0 Gestión del Proyecto** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 1.1 Acta de Constitución | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 1.2 Registro de Interesados | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 1.3 Documento de Requerimientos |  | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 1.4 Documento de Alcance y Gestión |  | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 1.5 Revisión de pares de los documentos de gestión |  | □ | □ | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **2.0 Diseño y Arquitectura** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 2.1 Definición de stack tecnológico |  |  | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 2.2 Modelo de datos genérico multirubro |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 2.3 Spike técnico homologación ARCA |  |  |  | ■ | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 2.4 Revisión del modelo de datos contra 2 rubros |  |  |  | □ | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **3.0 Módulo Productos y Stock** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 3.1 Alta/baja/modificación de productos |  |  |  |  |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 3.2 Categorías y variantes configurables |  |  |  |  |  |  |  |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 3.3 Control de inventario y ajustes |  |  |  |  |  |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 3.4 Alertas de stock mínimo |  |  |  |  |  |  |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 3.5 Pruebas funcionales de Productos y Stock |  |  |  |  |  |  |  |  |  |  |  |  | □ | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |
| **4.0 Módulo Facturación (ARCA)** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 4.1.1 Autenticación WSAA |  |  |  |  |  |  | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.1.2 Cacheo y renovación del ticket |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.1.3 Cliente WSFEv1 |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.2 Emisión de Factura A/B/C |  |  |  |  |  |  |  |  | ■ | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.3 Notas de Crédito/Débito |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.4 Errores de WS y logging seguro |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.5 Exportación de comprobantes PDF |  |  |  |  |  |  |  |  |  |  |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.6 Credenciales de producción |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |  |  |  |
| 4.7 Pruebas de integración contra homologación ARCA |  |  |  |  |  |  |  |  |  |  |  | □ | □ | □ | □ |  |  |  |  |  |  |  |  |  |  |  |  |
| **5.0 Clientes/Proveedores y Cuentas Corrientes** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 5.1 ABM clientes/proveedores |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |  |
| 5.2 Cuentas corrientes |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |  |
| 5.3 Consulta de estado de cuenta |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |
| 5.4 Pruebas funcionales de Clientes/Proveedores |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | □ | □ | □ |  |  |  |  |  |  |
| **6.0 Módulo Pagos y Giftcards** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 6.1.1 Efectivo y cuenta corriente |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |  |  |  |  |  |
| 6.1.2 Débito/crédito y transferencia |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | □ |  |  |  |  |  |  |  |  |  |  |  |
| 6.1.3 QR |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | □ |  |  |  |  |  |  |  |  |  |  |
| 6.2 Pago combinado / mixto |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |  |  |  |  |  |
| 6.3 Giftcards |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |  |
| 6.4 Pasarela simulada/sandbox |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | □ | □ |  |  |  |  |  |  |  |  |  |  |
| 6.5 Pruebas funcionales de Pagos y Giftcards |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | □ | □ | □ |  |  |  |  |  |  |
| **7.0 Módulo Reportes y Estadísticas** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 7.1 Ventas por período |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |  |
| 7.2 Productos más vendidos |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |  |  |  |
| 7.3 Stock crítico |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |  |
| 7.4 Cuentas corrientes |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |  |  |
| 7.5 Rentabilidad |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |  |
| 7.6 Exportación de reportes |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |  |
| 7.7 Pruebas funcionales de Reportes |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |
| **8.0 Módulo Usuarios y Permisos** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 8.1 Rol administrador |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |  |  |
| 8.2 Rol cajero |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |
| 8.3 Pruebas de permisos por rol |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |  |  |  |
| **9.0 Pruebas, Integración y Cierre** | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| 9.1 Ciclo integral |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |  |
| 9.2 Genericidad en ≥2 rubros |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ | ■ |  |
| 9.3 Validación final ARCA |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |  |
| 9.4 Entrega final y cierre |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | ■ |

## **5. Análisis de ruta crítica (CPM)**

*Duración lógica 19 sem. · Plan base 27 sem.*

Se aplicó el método de la ruta crítica (CPM) a la red de la Lista de Actividades v1.1, con las duraciones en semanas y la convención de la Lista (una actividad puede comenzar en la semana en que finaliza su predecesora). Resultado: la duración lógica mínima es de 19 semanas, con 33 de 48 actividades críticas (holgura 0).

| ID | Actividad | Dur. | IT | FT | IT tard. | FT tard. | Holg. | Crít. |
| :---- | :---- | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| 1.1 | Acta de Constitución | 1 | 1 | 1 | 1 | 1 | 0 | Sí |
| 1.2 | Registro de Interesados | 1 | 1 | 1 | 1 | 1 | 0 | Sí |
| 1.3 | Documento de Requerimientos | 1 | 1 | 1 | 1 | 1 | 0 | Sí |
| 1.4 | Documento de Alcance y Gestión | 1 | 1 | 1 | 1 | 1 | 0 | Sí |
| 1.5 | Revisión de pares de los documentos de gestión | 4 | 1 | 4 | 16 | 19 | 15 | No |
| 2.1 | Definición de stack tecnológico | 1 | 1 | 1 | 1 | 1 | 0 | Sí |
| 2.2 | Modelo de datos genérico multirubro | 2 | 1 | 2 | 2 | 3 | 1 | No |
| 2.3 | Spike técnico homologación ARCA | 3 | 1 | 3 | 1 | 3 | 0 | Sí |
| 2.4 | Revisión del modelo de datos contra 2 rubros | 3 | 2 | 4 | 17 | 19 | 15 | No |
| 3.1 | Alta/baja/modificación de productos | 2 | 3 | 4 | 14 | 15 | 11 | No |
| 3.2 | Categorías y variantes configurables | 2 | 4 | 5 | 16 | 17 | 12 | No |
| 3.3 | Control de inventario y ajustes | 2 | 4 | 5 | 15 | 16 | 11 | No |
| 3.4 | Alertas de stock mínimo | 2 | 5 | 6 | 16 | 17 | 11 | No |
| 3.5 | Pruebas funcionales de Productos y Stock | 3 | 6 | 8 | 17 | 19 | 11 | No |
| 4.1.1 | Autenticación WSAA | 1 | 3 | 3 | 3 | 3 | 0 | Sí |
| 4.1.2 | Cacheo y renovación del ticket | 2 | 3 | 4 | 3 | 4 | 0 | Sí |
| 4.1.3 | Cliente WSFEv1 | 2 | 4 | 5 | 4 | 5 | 0 | Sí |
| 4.2 | Emisión de Factura A/B/C | 3 | 5 | 7 | 5 | 7 | 0 | Sí |
| 4.3 | Notas de Crédito/Débito | 2 | 7 | 8 | 7 | 8 | 0 | Sí |
| 4.4 | Errores de WS y logging seguro | 2 | 8 | 9 | 8 | 9 | 0 | Sí |
| 4.5 | Exportación de comprobantes PDF | 2 | 7 | 8 | 18 | 19 | 11 | No |
| 4.6 | Credenciales de producción | 2 | 9 | 10 | 9 | 10 | 0 | Sí |
| 4.7 | Pruebas de integración contra homologación ARCA | 4 | 8 | 11 | 16 | 19 | 8 | No |
| 5.1 | ABM clientes/proveedores | 2 | 10 | 11 | 10 | 11 | 0 | Sí |
| 5.2 | Cuentas corrientes | 2 | 11 | 12 | 11 | 12 | 0 | Sí |
| 5.3 | Consulta de estado de cuenta | 2 | 12 | 13 | 12 | 13 | 0 | Sí |
| 5.4 | Pruebas funcionales de Clientes/Proveedores | 3 | 13 | 15 | 17 | 19 | 4 | No |
| 6.1.1 | Efectivo y cuenta corriente | 1 | 12 | 12 | 12 | 12 | 0 | Sí |
| 6.1.2 | Débito/crédito y transferencia | 1 | 10 | 10 | 11 | 11 | 1 | No |
| 6.1.3 | QR | 1 | 11 | 11 | 12 | 12 | 1 | No |
| 6.2 | Pago combinado / mixto | 1 | 12 | 12 | 12 | 12 | 0 | Sí |
| 6.3 | Giftcards | 2 | 12 | 13 | 12 | 13 | 0 | Sí |
| 6.4 | Pasarela simulada/sandbox | 2 | 10 | 11 | 11 | 12 | 1 | No |
| 6.5 | Pruebas funcionales de Pagos y Giftcards | 3 | 13 | 15 | 15 | 17 | 2 | No |
| 7.1 | Ventas por período | 2 | 13 | 14 | 13 | 14 | 0 | Sí |
| 7.2 | Productos más vendidos | 1 | 14 | 14 | 14 | 14 | 0 | Sí |
| 7.3 | Stock crítico | 2 | 14 | 15 | 14 | 15 | 0 | Sí |
| 7.4 | Cuentas corrientes | 1 | 15 | 15 | 15 | 15 | 0 | Sí |
| 7.5 | Rentabilidad | 2 | 15 | 16 | 15 | 16 | 0 | Sí |
| 7.6 | Exportación de reportes | 1 | 16 | 16 | 16 | 16 | 0 | Sí |
| 7.7 | Pruebas funcionales de Reportes | 2 | 16 | 17 | 16 | 17 | 0 | Sí |
| 8.1 | Rol administrador | 2 | 16 | 17 | 16 | 17 | 0 | Sí |
| 8.2 | Rol cajero | 1 | 17 | 17 | 17 | 17 | 0 | Sí |
| 8.3 | Pruebas de permisos por rol | 1 | 17 | 17 | 17 | 17 | 0 | Sí |
| 9.1 | Ciclo integral | 2 | 17 | 18 | 17 | 18 | 0 | Sí |
| 9.2 | Genericidad en ≥2 rubros | 2 | 18 | 19 | 18 | 19 | 0 | Sí |
| 9.3 | Validación final ARCA | 1 | 19 | 19 | 19 | 19 | 0 | Sí |
| 9.4 | Entrega final y cierre | 1 | 19 | 19 | 19 | 19 | 0 | Sí |

*IT/FT = inicio/fin más temprano; IT tard./FT tard. = inicio/fin más tardío para terminar en la semana 19; Holg. = holgura total en semanas. Todas las unidades son semanas del proyecto.*

## **6. Interpretación y carga de recursos**

*Ruta crítica · Capacidad.*

**Ruta crítica lógica** (de la que depende la fecha mínima de fin si los recursos no fueran una restricción): {1.1 ∥ 1.2} → 1.3 → 1.4 → 2.1 → 2.3 → 4.1.1 → 4.1.2 → 4.1.3 → 4.2 → 4.3 → 4.4 → 4.6 → 5.1 → 5.2 → {5.3 ∥ (6.1.1 → 6.2 → 6.3)} → 7.1 → 7.2 → 7.3 → 7.4 → 7.5 → 7.6 → {7.7 ∥ 8.1 → 8.2 → 8.3} → 9.1 → 9.2 → 9.3 → 9.4 (el símbolo ∥ indica ramas paralelas).

- La ruta atraviesa el paquete 4.0 Facturación (ARCA) completo (4.1.1 → 4.1.2 → 4.1.3 → 4.2 → 4.3 → 4.4 → 4.6) y se origina en el spike 2.3. Esto es coherente con la marca «Ruta crítica» de la Lista de Actividades y con el riesgo principal del Acta (complejidad de los WS de ARCA, ver Plan de Riesgos R1).
- El cronograma base dura 27 semanas, es decir 8 más que la duración lógica de 19. La diferencia no es un error: el calendario está dominado por la capacidad del equipo fijo (RNF-10): 970 h de esfuerzo esperado a 40 h/semana equivalen a 24,25 semanas, y 1.080 h de presupuesto a 40 h/semana equivalen exactamente a 27 semanas (ver Estimación y Presupuesto, §5).
- Las actividades 1.5 y 2.4 (revisiones de QA) y 3.2 son las de mayor holgura (ramas que no alimentan a otras), por lo que son las candidatas naturales para absorber desvíos de recursos; luego 4.5, 3.4 y 3.5.
- Las precedencias de la Lista son lógicas, salvo la compuerta de hito (5.1 y 6.1.2 requieren cerrar 4.6, y 9.1 requiere cerrar 8.2, 8.3, 7.7 y 6.5), que además refleja el reparto de personas.

**Carga semanal derivada del cronograma base.** Distribuyendo las horas esperadas de cada actividad de forma uniforme sobre sus semanas, la demanda del equipo supera la capacidad de 40 h/semana en 10 semanas (8, 9, 12, 13, 14, 17, 18, 19, 22, 23), con un pico de 47,8 h en la semana 13 (09/11/2026); en la versión 1.0 del cronograma el pico era de 83 h (semana 17). La nivelación de la versión 1.1 se hizo desplazando actividades con holgura dentro de su hito, sin modificar H1–H4. La demanda total de H2 (365 h) supera en 5 h su capacidad (360 h) y no puede nivelarse sin sacar horas: ese exceso se cubre con la reserva (Estimación y Presupuesto §5). Regla de seguimiento: ninguna semana planificada debe superar 50 h.

| Sem. | Horas | Sem. | Horas | Sem. | Horas |
| :---- | :----: | :---- | :----: | :---- | :----: |
| 1 | 16 | 10 | 32,3 | 19 | 40,8 |
| 2 | 32,8 | 11 | 36,8 | 20 | 37,3 |
| 3 | 28,8 | 12 | 41,2 | 21 | 37,8 |
| 4 | 38,1 | 13 | 47,8 | 22 | 41 |
| 5 | 24,1 | 14 | 47,8 | 23 | 44 |
| 6 | 20,3 | 15 | 39,2 | 24 | 22,5 |
| 7 | 35,5 | 16 | 25,5 | 25 | 37,5 |
| 8 | 42 | 17 | 41,5 | 26 | 40 |
| 9 | 42,3 | 18 | 47 | 27 | 30 |

## **7. Hitos y compuertas**

*H1 a H4.*

| Hito | Fecha objetivo | Condición de cumplimiento (verificada según Plan de Calidad, JJT-GPI-10 §7) | Origen |
| :---- | :---- | :---- | :---- |
| H1 | Semana 6 (27/09/2026) | Acta, Interesados, Requerimientos y Alcance emitidos y aprobados (1.1–1.4); revisión de pares (1.5); stack definido (2.1); modelo de datos genérico (2.2) revisado contra dos rubros (2.4); spike con conexión a homologación de ARCA documentado (2.3). | Alcance §3; Lista 1.0–2.0 |
| H2 | Semana 15 (29/11/2026) | Módulo Productos y Stock operativo y probado (3.x); facturación A/B/C y NC/ND con CAE obtenido en homologación (4.2, 4.3); errores y logging seguro (4.4); credenciales de producción configurables (4.6); pruebas de integración ARCA (4.7). | Criterio de éxito 1 (Alcance §6); RF-01 a RF-11 |
| H3 | Semana 23 (24/01/2027) | Clientes/Proveedores y cuentas corrientes (5.x); pagos y giftcards (6.x); reportes y exportación (7.x); roles administrador y cajero (8.x); pruebas funcionales de cada módulo (5.4, 6.5, 7.7, 8.3). | RF-12 a RF-30 |
| H4 | Semana 27 (21/02/2027) | Ciclo integral alta → venta → facturación → pago → reportes (9.1); genericidad en ≥2 rubros (9.2); validación final contra homologación (9.3); entrega final y cierre (9.4). | Criterios de éxito 2 y 3 (Alcance §6); RF-31, RF-32 |

*Estado al 06/10/2026 (semana 8): la fecha de la compuerta H1 (27/09/2026) ya pasó. Al cierre de esta revisión no hay en `docs/` evidencia de 1.5, 2.1, 2.2, 2.3 ni 2.4 ni de un acta de revisión de hito; el Plan de Proyecto (JJT-GPI-12, §5) las registra como pendientes de confirmar.*

