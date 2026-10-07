

# **Acta de Constitución del Proyecto**

*Sistema de Gestión y Facturación Ágil integrado con ARCA*

**Proyecto:** Sistema de Gestión y Facturación Ágil integrado con ARCA

**Nombre corto del proyecto:** *JJT Manager*

**Fecha de emisión:** 19/08/2026

**Código del documento:** JJT-GPI-01

**Versión del documento:** 1.3 (revisión del 07/10/2026, aprobada por el sponsor)

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 19/08/2026 | Emisión inicial. |
| 1.1 | 06/10/2026 | Fecha de fin y calendario aclarados; metodología con sprints; presupuesto desglosado por integrante e infraestructura (USD 27.025); reportes del alcance alineados con los objetivos (rentabilidad); correcciones de formato y ortografía. Los cambios de fecha y presupuesto requieren aprobación del sponsor (Documento de Alcance, §7). |
| 1.2 | 06/10/2026 | Se define la duración de los sprints (2 semanas; antes figuraba «[N]»). Se agrega el objetivo específico 7 (usuarios y permisos), que estaba en el alcance sin objetivo asociado, y el interesado Railway (proveedor de infraestructura), ya presente en el Registro de Interesados. El nombre de H3 incluye Usuarios y permisos. Se reformula el supuesto sobre la validación del sponsor y se ordenan las listas de restricciones, supuestos y autoridad. Se unifica la grafía «Tomás». Mantiene pendiente la aprobación del sponsor de los cambios de fecha y presupuesto de la v1.1. |
| 1.3 | 07/10/2026 | El objetivo 6 se alinea con los reportes del alcance (se quitan «clientes» y «medios de pago», que no estaban en el alcance ni en la EDT). El presupuesto declara que USD 27.000 es el techo de personal, con 970 h de línea base (USD 24.250) y 110 h de reserva (USD 2.750); los importes se unifican en formato USD y se corrige el título del total. Se define el rol del comerciante/usuario final. Se anidan las listas de §4. El Sponsor aprobó el Acta, incluidos los cambios de fecha de fin y de presupuesto introducidos desde la v1.1 (aprobación confirmada por el equipo; fecha de firma a registrar en §12). |

1. ### **Datos generales**

| Campo | Detalle |
| :---- | :---- |
| Patrocinador (Sponsor) | Julio Gutierrez |
| Director de proyecto | *Tomás Disandro* |
| Equipo del proyecto | Juan Cruz Bulatovich: Frontend; Jesus Manuel Martinez: QA y QC; Tomás Disandro: Backend |
| Fecha de inicio | 19/08/2026 |
| Fecha estimada de fin | 21/02/2027 (27 semanas de proyecto, contadas desde el lunes 17/08/2026, semana en que inicia el proyecto) |
| Metodología de gestión | Híbrida: enfoque predictivo para planificación y documentación, y desarrollo iterativo en sprints de 2 semanas en H2 y H3 (el último sprint de H2 dura 3 semanas; ver Documento de Alcance §3.1) |

2. ### **Propósito y justificación del proyecto**

Pequeños y medianos comercios (kioscos, almacenes, supermercados de barrio, tiendas de indumentaria, ferreterías, etc.) necesitan una herramienta única que integre **control de stock, facturación electrónica válida ante ARCA, gestión de clientes y proveedores, cuentas corrientes, múltiples medios de pago y reportes**, sin depender de múltiples sistemas desconectados entre sí ni de soluciones sobredimensionadas y costosas pensadas para grandes cadenas.

3. ### **Objetivos del proyecto**

   1. #### **Objetivo general**

Desarrollar un sistema de gestión comercial multirubro que permita administrar stock, facturar electrónicamente mediante integración con ARCA, gestionar clientes/proveedores/cuentas corrientes, aceptar múltiples medios de pago (incluyendo giftcards) y generar reportes y estadísticas de negocio.

2. #### **Objetivos específicos**

   1. Diseñar un modelo de datos genérico, adaptable a distintos rubros comerciales (no atado a un tipo de negocio específico).

   2. Implementar facturación electrónica integrada con los Web Services de ARCA, soportando certificados de homologación (testing) y de producción (credenciales reales).

   3. Desarrollar módulo de control de stock con alta/baja/modificación de productos, categorías, variantes y alertas de stock mínimo.

   4. Desarrollar módulo de clientes y proveedores con gestión de cuentas corrientes (saldo, movimientos, límites de crédito).

   5. Soportar múltiples medios de pago (efectivo, tarjeta débito/crédito, transferencia, QR, cuenta corriente) y gestión de giftcards (emisión, carga, canje, saldo).

   6. Generar reportes y estadísticas (ventas por período, productos más vendidos, stock crítico, estado de cuentas corrientes y rentabilidad) exportables.

   7. Implementar usuarios y permisos con roles básicos (administrador y cajero).

4. ### **Alcance de alto nivel**

   1. #### **Incluido (in scope)**

   * Módulo de **Productos y Stock**: catálogo, categorías, variantes, control de inventario, ajustes de stock, alertas.

   * Módulo de **Facturación** con integración a ARCA (Factura A/B/C, notas de crédito/débito, homologación y producción).

   * Módulo de **Clientes** y **Proveedores** con datos fiscales y cuentas corrientes.

   * Módulo de **Pagos**: múltiples medios de pago por venta, combinación de medios (pago mixto).

   * Módulo de **Giftcards**: emisión, recarga, canje, consulta de saldo.

   * Módulo de **Reportes y Estadísticas**: ventas por período, productos más vendidos, stock crítico, estado de cuentas corrientes, rentabilidad.

   * Módulo de **Usuarios y permisos** (roles básicos: administrador, cajero).

   * Diseño genérico y configurable para distintos rubros (parametrización de catálogo, sin lógica específica de un solo tipo de comercio).

   2. #### **Excluido (out of scope) — para esta entrega**

   * Aplicación móvil nativa (se contempla diseño responsive web, no app store).

   * Integración con múltiples pasarelas de pago en producción (se implementa una simulada/sandbox).

   * Multi-sucursal / multi-empresa avanzado (franquicias, consolidación entre locales).

   * Módulo de e-commerce / venta online integrada.

   * Soporte multiidioma / multimoneda.

   * Integración con hardware fiscal específico (impresoras fiscales homologadas físicas) más allá de impresión estándar de comprobantes en PDF.

*(Este límite se detalla y puede ajustarse en el Documento de Alcance — sección control de cambios.)*

5. ### **Interesados (Stakeholders) principales**

| Stakeholder | Rol / interés |
| :---- | :---- |
| Julio Gutierrez | Cliente |
| Equipo del proyecto (3 integrantes) | Ejecutores: desarrollo, gestión y documentación |
| Comerciante/usuario final (perfil representativo; lo cubre un comerciante a designar por el Sponsor) | Usuario objetivo del producto; valida usabilidad y utilidad en las demostraciones de cierre de H2, H3 y H4 |
| ARCA (organismo fiscal) | Define las reglas y Web Services con los que el sistema debe interoperar |
| Railway (proveedor de infraestructura) | Provee el servidor sobre el que corre el sistema (costo en el presupuesto) |

6. ### **Riesgos de alto nivel identificados**

| Riesgo | Impacto | Probabilidad | Estrategia inicial |
| :---- | :---- | :---- | :---- |
| Complejidad/documentación insuficiente de los WS de ARCA | Alto | Media | Reservar tiempo temprano para spike técnico de homologación; usar librerías de terceros probadas si existen |
| Cambios de alcance no controlados (“scope creep”) por ser un dominio muy amplio (multirubro) | Medio | Alta | Proceso formal de control de cambios (ver Documento de Alcance) |

7. ### **Hitos principales (alto nivel)**

| Hito | Descripción | Semana estimada |
| :---- | :---- | :---- |
| H1 | Planificación, arquitectura y diseño | Semanas 1-6 |
| H2 | Desarrollo del sistema central (Stock y Facturación ARCA) | Semanas 7-15 |
| H3 | Desarrollo de módulos complementarios (Clientes, Pagos, Reportes y Usuarios) | Semanas 16-23 |
| H4 | Pruebas, integración y entrega final | Semanas 24-27 |

8. ### **Presupuesto de alto nivel**

**Costos de Infraestructura:**

* Railway (Servidor): USD 5 mensuales × 5 meses (oct/2026–feb/2027; contratación al inicio de H2, semana 7, con primer cobro en octubre) = USD 25.

**Costos de Personal:**

* Tomás Disandro: 360 horas × USD 25/hora = USD 9.000

* Juan Cruz Bulatovich: 360 horas × USD 25/hora = USD 9.000

* Jesus Manuel Martinez: 360 horas × USD 25/hora = USD 9.000

*(El reparto de horas por integrante es una propuesta a confirmar por el Director de Proyecto; el desglose por actividad y por rol está en el documento de Estimación y Presupuesto, JJT-GPI-08.)*

**Costos totales (personal e infraestructura):**

* Subtotal de personal: 1.080 horas = USD 27.000. Es el **techo** de personal: la estimación vigente es de 970 horas de línea base (USD 24.250, BAC) más 110 horas de reserva (USD 2.750).

* Infraestructura: USD 25

* **Total general: USD 27.025**

9. ### **Criterios de éxito**

1. El sistema emite facturas electrónicas válidas contra el ambiente de homologación de ARCA (CAE obtenido correctamente).

2. El sistema permite operar el ciclo completo: alta de producto → venta con control de stock → facturación → registro de pago → impacto en reportes.

3. El modelo de datos demuestra ser aplicable a al menos 2 rubros distintos (ej. kiosco y tienda de indumentaria) sin cambios de código, sólo de configuración/datos.

10. ### **Restricciones y supuestos**

**Restricciones:**

* Equipo fijo de 3 personas sin posibilidad de incorporar recursos adicionales.

* Uso obligatorio de certificados de testing de ARCA para desarrollo; credenciales reales solo para validación final opcional.

**Supuestos:**

* ARCA mantiene disponible y estable su ambiente de homologación durante el desarrollo.

* El equipo cuenta con acceso a una CUIT de prueba habilitada para generar certificados de testing.

* El sponsor valida los entregables del producto y la documentación de gestión en cada hito.

11. ### **Autoridad del Director de Proyecto**

El Director de Proyecto **Tomás Disandro** está autorizado a:

* Asignar tareas dentro del equipo.

* Priorizar el backlog en conjunto con el equipo.

* Proponer cambios de alcance siguiendo el proceso de control de cambios.

* Representar al equipo ante el sponsor para reportar avance.

12. ### **Aprobación**

*Aprobada por el Sponsor, incluidos los cambios de fecha de fin y de presupuesto de la v1.1 (confirmado por el equipo). Falta registrar la firma y la fecha de cada persona en la tabla.*

| Rol | Nombre | Firma / Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Sponsor | Julio Gutierrez | | |
| Integrante 1 | Juan Cruz Bulatovich | | |
| Integrante 2 | Jesus Manuel Martinez | | |
| Integrante 3 | Tomás Disandro | | |
