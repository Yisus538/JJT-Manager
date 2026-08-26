

DOCUMENTO DE  GESTIÓN DE PROYECTOS

# **Alcance y Gestión** 

Sistema de Gestión y Facturación Ágil integrado con ARCA

Nombre corto del proyecto	**JJT Manager**

Patrocinador (Sponsor)	**Julio Gutierrez**

Director de proyecto	**Tomas Disandro**

Fecha	**25/08/2026**

## **Documento de Alcance y Gestión GPI**

**Proyecto:** Sistema de Gestión y Facturación Ágil integrado con ARCA (JJT Manager)

**Fecha:** 25/08/2026

> Este documento desarrolla el **alcance de alto nivel** del Acta de Constitución en una Declaración de Alcance, una Estructura de Desglose del Trabajo (EDT), un cronograma de hitos y sprints, y el **proceso formal de control de cambios** (sección 7) al que debe someterse cualquier pedido que exceda lo aquí definido. Cada apartado cita la sección del Acta o del Documento de Requerimientos de la que se deriva.

1. ### **Declaración de alcance**

   1. #### **Incluido (in scope)**

| Módulo | Detalle | Trazabilidad |
| :---- | :---- | :---- |
| **Incluido** | **Productos y Stock:** catálogo, categorías y variantes configurables, control de inventario, ajustes de stock, alertas de stock mínimo. | RF-01 a RF-05 |
| **Incluido** | **Facturación (ARCA):** Factura A/B/C, Notas de Crédito/Débito, ambientes de homologación y producción configurables. | RF-06 a RF-11 |
| **Incluido** | **Clientes y Proveedores:** datos fiscales, cuentas corrientes (saldo, movimientos, límite de crédito). | RF-12 a RF-14 |
| **Incluido** | **Pagos y Giftcards:** medios de pago múltiples y combinables, emisión/recarga/canje/consulta de giftcards. | RF-15 a RF-21 |
| **Incluido** | **Reportes y Estadísticas:** ventas, productos más vendidos, stock crítico, cuentas corrientes, rentabilidad, exportación. | RF-22 a RF-27 |
| **Incluido** | **Usuarios y permisos:** roles administrador y cajero. | RF-28 a RF-30 |
| **Incluido** | **Genericidad multirubro:** modelo de datos aplicable a ≥2 rubros sin cambios de código. | RF-32; RNF-01 a RNF-03 |

   2. #### **Excluido (out of scope) — para esta entrega**

| Módulo | Detalle | Trazabilidad |
| :---- | :---- | :---- |
| **Excluido** | Aplicación móvil nativa (se contempla diseño responsive web, no app store). | RNF-06 |
| **Excluido** | Integración con múltiples pasarelas de pago en producción (se implementa una simulada/sandbox). | RF-21 |
| **Excluido** | Multi-sucursal / multi-empresa avanzado (franquicias, consolidación entre locales). | RNF-07 |
| **Excluido** | Módulo de e-commerce / venta online integrada. | RNF-07 |
| **Excluido** | Soporte multiidioma / multimoneda. | RNF-07 |
| **Excluido** | Integración con hardware fiscal físico homologado, más allá de impresión estándar de comprobantes en PDF. | RF-11; RNF-07 |

2. ### **Estructura de Desglose del Trabajo (EDT)**

La EDT organiza el trabajo en 4 fases, alineadas a los hitos de alto nivel del Acta (H1-H4) y ordenadas siguiendo la prioridad de módulos: Productos/Stock → Facturación/ARCA → Clientes/CtaCte → Pagos/Giftcards → Reportes.

#### **1.0 Gestión del Proyecto**

* 1.1 Acta de Constitución
* 1.2 Registro de Interesados
* 1.3 Documento de Requerimientos
* 1.4 Documento de Alcance y Gestión (este documento)

#### **2.0 Diseño y Arquitectura**

* 2.1 Definición de stack tecnológico
* 2.2 Modelo de datos genérico multirubro (RNF-01 a RNF-03)
* 2.3 Spike técnico de homologación con Web Services de ARCA (mitigación de riesgo, Acta y Riesgos)

#### **3.0 Módulo Productos y Stock**

* 3.1 Alta/baja/modificación de productos (RF-01)
* 3.2 Categorías y variantes configurables (RF-02, RF-03)
* 3.3 Control de inventario y ajustes de stock (RF-04)
* 3.4 Alertas de stock mínimo (RF-05)

#### **4.0 Módulo Facturación (ARCA)**

* 4.1 Integración WSAA/WSFEv1 — ambiente de homologación (RF-06, RF-08)
* 4.2 Emisión de Factura A/B/C (RF-06)
* 4.3 Notas de Crédito/Débito (RF-07)
* 4.4 Manejo de errores de WS y logging seguro (RF-09, RF-10, RNF-04, RNF-05)
* 4.5 Exportación de comprobantes en PDF (RF-11)
* 4.6 Habilitación de credenciales de producción configurables (RF-08)

#### **5.0 Módulo Clientes/Proveedores y Cuentas Corrientes**

* 5.1 ABM de clientes y proveedores con datos fiscales (RF-12)
* 5.2 Cuentas corrientes: saldo, movimientos, límite de crédito (RF-13)
* 5.3 Consulta de estado de cuenta (RF-14)

#### **6.0 Módulo Pagos y Giftcards**

* 6.1 Medios de pago múltiples: efectivo, débito/crédito, transferencia, QR, cuenta corriente (RF-15)
* 6.2 Pago combinado / mixto (RF-16)
* 6.3 Giftcards: emisión, recarga, canje, consulta de saldo (RF-17 a RF-20)
* 6.4 Integración con pasarela simulada/sandbox (RF-21)

#### **7.0 Módulo Reportes y Estadísticas**

* 7.1 Reporte de ventas por período (RF-22)
* 7.2 Reporte de productos más vendidos (RF-23)
* 7.3 Reporte de stock crítico (RF-24)
* 7.4 Reporte de cuentas corrientes (RF-25)
* 7.5 Reporte de rentabilidad (RF-26)
* 7.6 Exportación de reportes (RF-27)

#### **8.0 Módulo Usuarios y Permisos**

* 8.1 Rol administrador (RF-29)
* 8.2 Rol cajero (RF-30)

#### **9.0 Pruebas, Integración y Cierre**

* 9.1 Prueba de ciclo integral: alta de producto → venta → facturación → pago → reportes (RF-31)
* 9.2 Validación de genericidad en ≥2 rubros (RF-32)
* 9.3 Validación final contra ambiente de homologación de ARCA (Acta y Criterios de éxito)
* 9.4 Entrega final y documentación de cierre

3. ### **Cronograma de hitos**

| Hito  | Descripción | Semana estimada | EDT asociada |
| :---- | :---- | :---- | :---- |
| **H1** | Planificación, arquitectura y diseño | Semanas 1-6 | 1.0, 2.0 |
| **H2** | Desarrollo del sistema central (Stock y Facturación ARCA) | Semanas 7-15 | 3.0, 4.0 |
| **H3** | Desarrollo de módulos complementarios (Clientes, Pagos y Reportes) | Semanas 16-23 | 5.0, 6.0, 7.0, 8.0 |
| **H4** | Pruebas, integración y entrega final | Semanas 24-27 | 9.0 |

   1. #### **Metodología de gestión**

El proyecto sigue una metodología **híbrida**: fases predictivas para planificación y documentación de gestión (H1), y desarrollo iterativo por sprints, cerrando con una fase predictiva de estabilización y entrega (H4).

4. ### **Equipo y responsabilidades**

| Integrante | Rol | Frentes EDT bajo su responsabilidad principal |
| :---- | :---- | :---- |
| Tomas Disandro | Director de Proyecto / Backend | 1.0, 2.0, 4.0, 5.0 |
| Juan Cruz Bulatovich | Frontend | 3.0, 6.0, 7.0, 8.0 (interfaces) |
| Jesus Manuel Martinez | QA y QC | 9.0 (pruebas e integración, transversal a todos los módulos) |

5. ### **Riesgos de alto nivel**

| Riesgo | Impacto | Probabilidad | Estrategia inicial |
| :---- | :---- | :---- | :---- |
| Complejidad/documentación insuficiente de los WS de ARCA | Alto | Media | Reservar tiempo temprano para spike técnico de homologación (EDT 2.3); usar librerías de terceros probadas si existen. |
| Cambios de alcance no controlados ("scope creep") por ser un dominio muy amplio (multirubro) | Medio | Alta | Proceso formal de control de cambios (ver sección 7). |

6. ### **Criterios de éxito y restricciones**

   1. #### **Criterios de éxito**

      * El sistema emite facturas electrónicas válidas contra el ambiente de homologación de ARCA (CAE obtenido correctamente). *(RF-06, RF-08, RF-09)*

      * El sistema permite operar el ciclo completo: alta de producto → venta con control de stock → facturación → registro de pago → impactó en reportes. *(RF-31)*

      * El modelo de datos demuestra ser aplicable a al menos 2 rubros distintos (ej. kiosco y tienda de indumentaria) sin cambios de código, sólo de configuración/datos. *(RF-32)*

   2. #### **Restricciones**

      * Equipo fijo de 3 personas sin posibilidad de incorporar recursos adicionales. *(RNF-10)*

      * Uso obligatorio de certificados de testing de ARCA para desarrollo; credenciales reales solo para validación final opcional. *(RNF-09)*

   3. #### **Supuestos**

      * ARCA mantiene disponible y estable su ambiente de homologación durante el desarrollo.

      * El equipo cuenta con acceso a una CUIT de prueba habilitada para generar certificados de testing.

7. ### **Proceso de control de cambios**

Cualquier solicitud que agregue, quite o modifique un ítem del alcance definido en la sección 1 (incluido/excluido) debe pasar por este proceso antes de implementarse. El objetivo es mitigar el riesgo de "scope creep" identificado en la sección 5.

   1. #### **Pasos del proceso**

   1. **Registro de la solicitud:** quien propone el cambio (equipo o sponsor) lo documenta por escrito: qué se pide, por qué, y qué ítem del alcance actual afecta.

   2. **Análisis de impacto:** el Director de Proyecto, junto al equipo, evalúa impacto en cronograma (hitos H1-H4), presupuesto (horas/costo), y en el modelo de datos genérico (¿introduce lógica específica de un rubro?).

   3. ##### **Decisión:**

      * Si el cambio es menor y no desplaza hitos ni introduce lógica no genérica: puede aprobarlo el Director de Proyecto e informar al equipo.

      * Si el cambio es significativo (afecta fecha de fin, presupuesto, o alguno de los ítems marcados "Excluido" en la sección 1.2): requiere aprobación explícita del Sponsor (Julio Gutierrez).

   4. **Actualización de documentación:** de aprobarse, se actualiza este documento (Declaración de alcance, EDT y/o cronograma), el Documento de Requerimientos, y se incrementa la versión de ambos documentos.

   5. **Comunicación:** el cambio aprobado y su justificación se comunican a todo el equipo antes de iniciar su desarrollo.
