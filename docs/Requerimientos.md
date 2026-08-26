

DOCUMENTO  DE  GESTIÓN  DE  PROYECTOS

# **Documento de Requerimientos**

Sistema de Gestión y Facturación Ágil integrado con ARCA

Nombre corto del proyecto	**JJT Manager**

Patrocinador (Sponsor)	**Julio Gutierrez**

Director de proyecto	**Tomas Disandro**

Fecha	**25/08/2026**

## **Documento de Requerimientos**

**Proyecto:** Sistema de Gestión y Facturación Ágil integrado con ARCA (JJT Manager)

**Fecha:** 25/08/2026 

1. ### **Requerimientos funcionales**

   1. #### **Productos y Stock**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-01 | El sistema debe permitir el alta, baja y modificación de productos. | **Alta** | Acta y Alcance in-scope |
| RF-02 | El sistema debe permitir organizar productos en categorías definibles por el usuario, sin categorías fijas de un rubro específico. | **Alta** | Acta y Objetivos específicos;  |
| RF-03 | El sistema debe permitir definir variantes de producto (ej. talle, color, presentación) mediante atributos configurables, no columnas fijas. | **Alta** | Acta y Objetivos específicos |
| RF-04 | El sistema debe llevar el control de inventario (stock actual por producto/variante) y permitir ajustes manuales de stock con motivo registrado. | **Alta** | Acta y Alcance in-scope |
| RF-05 | El sistema debe emitir alertas de stock mínimo configurable por producto. | **Media** | Acta y Objetivos específicos |

   2. #### **Facturación electrónica (ARCA)**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-06 | El sistema debe emitir comprobantes de Factura A, B y C mediante integración con los Web Services de ARCA. | **Alta** | Acta y Alcance in-scope |

| RF-07 | El sistema debe permitir emitir Notas de Crédito y Notas de Débito asociadas a comprobantes previos. | Alta | Alcance in-scope |
| :---- | :---- | :---- | ----- |
| RF-08 | El sistema debe soportar certificados de homologación (testing) de ARCA por defecto en desarrollo, y credenciales de producción configurables sin hardcodear el ambiente. | **Alta** | ARCA |
| RF-09 | El sistema debe manejar explícitamente los errores devueltos por los WS de ARCA y no asumir que el CAE siempre se obtiene. |  **Alta** | ARCA |
| RF-10 | El sistema debe registrar (loguear) las respuestas de ARCA para depuración, sin exponer credenciales ni certificados en logs ni en el repositorio. | **Alta** | ARCA |
| RF-11 | El sistema debe permitir la impresión/exportación estándar de comprobantes en PDF. |  **Media** | Acta y Alcance out-of-scope (PDF sí incluido) |

3. #### **Clientes y Proveedores**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-12 | El sistema debe permitir el alta, baja y modificación de clientes y proveedores con sus datos fiscales. |  **Alta** | Acta y Alcance in-scope |
| RF-13 | El sistema debe gestionar cuentas corrientes por cliente/proveedor: saldo, historial de movimientos y límite de crédito. | **Alta** | Acta y Objetivos específicos |
| RF-14 | El sistema debe permitir consultar el estado de cuenta corriente de un cliente o proveedor en un momento dado. | **Media** | Acta y Alcance in-scope |

   4. #### **Pagos y Giftcards**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-15 | El sistema debe soportar múltiples medios de pago por venta: efectivo, tarjeta débito/crédito, transferencia, QR y cuenta corriente. |  **Alta** | Acta y Objetivos específicos |
| RF-16 | El sistema debe permitir combinar más de un medio de pago en una misma venta (pago mixto). | **Alta** | Acta y Alcance in-scope |
| RF-17 | El sistema debe permitir emitir giftcards. | **Media** | Acta y Objetivos específicos |

| RF-18 | El sistema debe permitir recargar saldo a una giftcard existente. | Media | Acta y Alcance in-scope |
| :---- | :---- | :---- | :---- |
| RF-19 | El sistema debe permitir canjear (usar como medio de pago) el saldo de una giftcard. | **Media** | Acta y Alcance in-scope |
| RF-20 | El sistema debe permitir consultar el saldo disponible de una giftcard. | **Media** | Acta y Alcance in-scope |
| RF-21 | La integración de medios de pago en producción se implementa contra una pasarela simulada/sandbox; no se integran múltiples pasarelas reales en esta entrega. | **Restricción** | Acta y Alcance out-of-scope |

5. #### **Reportes y Estadísticas**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-22 | El sistema debe generar reportes de ventas por período. | **Alta** | Acta y Alcance in-scope |
| RF-23 | El sistema debe generar reportes de productos más vendidos. | **Media** | Acta y Alcance in-scope |
| RF-24 | El sistema debe generar reportes de stock crítico (por debajo del mínimo). | **Media** | Acta y Alcance in-scope |
| RF-25 | El sistema debe generar reportes de estado de cuentas corrientes. | **Media** | Acta y Alcance in-scope |
| RF-26 | El sistema debe generar reportes de rentabilidad. | **Media** | Acta y Objetivos específicos |
| RF-27 | Los reportes deben poder exportarse (ej. PDF/CSV). | **Media** | Acta y Objetivos específicos |

   6. #### **Usuarios y permisos**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-28 | El sistema debe soportar al menos dos roles de usuario: administrador y cajero. | **Alta** | Acta y Alcance in-scope |
| RF-29 | El rol administrador debe tener acceso a la configuración del sistema, gestión de usuarios y reportes completos. | **Alta** | Acta y Alcance in-scope |
| RF-30 | El rol cajero debe poder operar el flujo de venta (stock, facturación, cobro) sin acceso a configuración sensible. | **Alta** | Acta y Alcance in-scope |

   7. #### **Flujo integral (criterio de éxito)**

| ID | Requerimiento | Prioridad | Fuente |
| :---- | :---- | :---- | :---- |
| RF-31 | El sistema debe soportar el ciclo completo: alta de producto → venta con control de stock → facturación → registro de pago → impacto en reportes, de forma consistente. | **Alta** | Acta y Criterios de éxito |
| RF-32 | El modelo de datos debe ser aplicable a al menos 2 rubros distintos (ej. kiosco y tienda de indumentaria) sin cambios de código, solo de configuración/datos. |  **Alta** | Acta y Criterios de éxito;  |

2. ### **Requerimientos no funcionales**

| ID | Requerimiento | Categoría | Fuente |
| :---- | :---- | :---- | :---- |
| RNF-01 | El sistema no debe hacer que el modelo de datos y la lógica de negocio asuman un rubro comercial específico  | Genericidad | Genericidad multirubro |
| RNF-02 | El sistema  debe hacer atributos de producto (variantes, categorías) configurables/extensibles por el usuario, no fijos en el esquema. | Genericidad | Genericidad multirubro |
| RNF-03 | El sistema  debe permitir  que el IVA y los tipos de comprobante sean parametrizables. | Genericidad | Genericidad multirubro |
| RNF-04 | El sistema no debe nunca commitearse al repositorio certificados (.crt/.key), CUIT reales ni credenciales de producción; deben gestionarse vía variables de entorno o archivos ignorados por git. | Seguridad | ARCA |
| RNF-05 | El sistema no debe hacer las credenciales/certificados exponerse en logs de la aplicación. | Seguridad | ARCA |
| RNF-06 | El sistema debe operar con una interfaz web responsive (no se contempla app móvil nativa en esta entrega). | Usabilidad | Acta y Alcance out-of-scope |
| RNF-07 | El sistema no contempla en esta entrega: multi-sucursal/multi-empresa avanzado, e-commerce, multi-idioma/multi-moneda, ni integración con hardware fiscal físico homologado. | Alcance | Acta y Alcance out-of-scope |

| RNF-08 | Cualquier requerimiento nuevo que contradiga el alcance definido debe pasar por el proceso formal de control de cambios antes de implementarse. | Gestión | Acta y Riesgos;  |
| :---- | :---- | :---- | :---- |
| RNF-09 | El desarrollo debe usar certificados de testing/homologación de ARCA por defecto; las credenciales reales de producción se usan solo para validación final opcional. | Restricción | Acta y Restricciones y supuestos |
| RNF-10 | El equipo de desarrollo es fijo (3 personas) durante todo el proyecto, sin incorporación de recursos adicionales. | Restricción | Acta y Restricciones y supuestos |

3. ### **Supuestos**

* ARCA mantiene disponible y estable su ambiente de homologación durante el desarrollo.

* El equipo cuenta con acceso a una CUIT de prueba habilitada para generar certificados de testing.

4. ### **Trazabilidad con hitos**

| Hito | Requerimientos asociados |
| :---- | :---- |
| **H1** — Planificación, arquitectura y diseño (semanas 1-6) | RNF-01 a RNF-03, RNF-08 |
| **H2** — Desarrollo del sistema central: Stock y Facturación ARCA (semanas 7-15) | RF-01 a RF-11 |
| **H3** — Módulos complementarios: Clientes, Pagos y Reportes (semanas 16-23) | RF-12 a RF-30 |
| **H4** — Pruebas, integración y entrega final (semanas 24-27) | RF-31, RF-32 |

