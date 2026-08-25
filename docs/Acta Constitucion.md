

# **Acta de Constitución del Proyecto**

*Sistema de Gestión y Facturación Ágil integrado con ARCA*

**Fecha:** 19/08/2026

**Versión del documento:** 1.0

## **Acta de Constitución del Proyecto**

**Proyecto:** Sistema de Gestión y Facturación Ágil integrado con ARCA 

**Nombre corto del proyecto:**  *JJT Manager* 

**Fecha:** 19/08/2026 

**Versión del documento:** 1.0

1. ### **Datos generales**

| Campo | Detalle |
| :---- | :---- |
| Patrocinador (Sponsor) | Julio Gutierrez |
| Director de proyecto | *Tomas Disandro* |
| Equipo del proyecto | Juan Cruz Bulatovich: Frontend Jesus Manuel Martines: QA y QC Tomas Disandro: Backend |
| Fecha de inicio | 19/08/2026 |
| Fecha estimada de fin | \~21/02/2027 |
| Metodología de gestión | Híbrida: fases predictivas para planificación/documentación y  desarrollo |

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

      6. Generar reportes y estadísticas (ventas, stock, rentabilidad, clientes, medios de pago) exportables.

4. ### **Alcance de alto nivel**

   1. #### **Incluido (in scope)**

* Módulo de **Productos y Stock**: catálogo, categorías, variantes, control de inventario, ajustes de stock, alertas.

* Módulo de **Facturación** con integración a ARCA (Factura A/B/C, notas de crédito/débito, homologación y producción).

* Módulo de **Clientes** y **Proveedores** con datos fiscales y cuentas corrientes.

* Módulo de **Pagos**: múltiples medios de pago por venta, combinación de medios (pago mixto).

* Módulo de **Giftcards**: emisión, recarga, canje, consulta de saldo.

* Módulo de **Reportes y Estadísticas**: ventas por período, productos más vendidos, stock crítico, estado de cuentas corrientes.

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
| Comerciante/usuario final (perfil hipotético representativo) | Usuario objetivo del producto; valida usabilidad y utilidad del sistema |
| ARCA (organismo fiscal) | Define las reglas y Web Services con los que el sistema debe interoperar |

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
| H3 | Desarrollo de módulos complementarios (Clientes, Pagos y Reportes) | Semanas 16-23 |
| H4 | Pruebas, integración y entrega final | Semanas 24-27 |

8. ### **Presupuesto de alto nivel**

**Costos de Infraestructura:**

* Railway (Servidor): 5 dólares mensuales.

**Costos de Personal :**

* Jesus Manuel Martinez: 25 dólares/hora

* Tomas Disandro: 25 dólares/hora

* Juan Cruz Bulatovich: 25 dólares/hora

**Costos totales basado en las horas de trabajo:**

* 1080 horas \= 27000 dólares

9.  **Criterios de éxito**

1. El sistema emite facturas electrónicas válidas contra el ambiente de homologación de ARCA (CAE obtenido correctamente).

2. El sistema permite operar el ciclo completo: alta de producto → venta con control de stock → facturación → registro de pago → impactó en reportes.

3. El modelo de datos demuestra ser aplicable a al menos 2 rubros distintos (ej. kiosco y tienda de indumentaria) sin cambios de código, sólo de configuración/datos.

10. ### **Restricciones y supuestos**

**Restricciones:** \-Equipo fijo de 3 personas sin posibilidad de incorporar recursos adicionales. \- Uso obligatorio de certificados de testing de ARCA para desarrollo; credenciales reales solo para validación final opcional.

**Supuestos:** \- ARCA mantiene disponible y estable su ambiente de homologación durante el desarrollo. \- El equipo cuenta con acceso a una CUIT de prueba habilitada para generar certificados de testing. \- El sponsor evalúa tanto el producto de software como el proceso de gestión aplicado.

11. ### **Autoridad del Director de Proyecto**

El Director de Proyecto **Tomas Disandro**  está autorizado a: \- Asignar tareas dentro del equipo. \- Priorizar el backlog en conjunto con el equipo. \- Proponer cambios de alcance siguiendo el proceso de control de cambios. \- Representar al equipo ante el sponsor para reportar avance.

> 12. ### **Aprobación**

| Rol | Nombre | Firma / Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Sponsor  | Julio gutierrez |  | 19/08/2026 |
| Integrante 1 | Juan Cruz Bulatovich |  | 19/08/2026 |
| Integrante 2 | Jesus Manuel Martinez |  | 19/08/2026 |
| Integrante 3 | Tomas Disandro |  | 19/08/2026 |

