

DOCUMENTO DE  GESTIÓN DE PROYECTOS

# **Lista de Actividades**

Sistema de Gestión y Facturación Ágil integrado con ARCA

Nombre corto del proyecto	**JJT Manager**

Código del documento	**JJT-GPI-06**

Patrocinador (Sponsor)	**Julio Gutierrez**

Director de proyecto	**Tomás Disandro**

Fecha	**26/08/2026** (versión 1.1: 06/10/2026)

## **Lista de Actividades**

**Proyecto:** Sistema de Gestión y Facturación Ágil integrado con ARCA (JJT Manager)

**Versión del documento:** 1.1 (06/10/2026)

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 26/08/2026 | Emisión inicial: 40 actividades en 9 paquetes. |
| 1.1 | 06/10/2026 | Se incorporan 8 actividades de QA por módulo (1.5, 2.4, 3.5, 4.7, 5.4, 6.5, 7.7, 8.3; total 48), de modo que la participación transversal de QA/QC prevista en el Alcance §4 quede programada. Se corrigen dependencias lógicas invertidas en el paquete 6.0 (la pasarela 6.4 precede al QR 6.1.3; el cobro a cuenta corriente 6.1.1 sigue a 5.2) y se elimina la precedencia 3.4 → 5.1 por no tener justificación lógica. Se nivela la carga semanal moviendo actividades con holgura, sin modificar los hitos H1–H4. Las horas por actividad se redistribuyen dentro de cada paquete (los totales por paquete no cambian). |

> Esta lista descompone cada paquete de trabajo de la EDT (`docs/EDT.md`) en sus actividades de nivel más bajo — las unidades programables del cronograma — con responsable, descripción, predecesoras y duración estimada. Las descripciones remiten, cuando corresponde, a los requerimientos funcionales/no funcionales de `docs/Requerimientos.md` (RF-XX / RNF-XX). Las duraciones y precedencias son una **estimación del equipo**, elaborada a partir del cronograma de hitos vigente (Documento de Alcance, §3); quedan sujetas al proceso formal de control de cambios (Documento de Alcance, §7) si se ajustan. Convención: una actividad puede comenzar en la semana en que finaliza su predecesora. Los IDs identifican la actividad en la EDT y no siempre siguen el orden cronológico (p. ej., en 6.0 la pasarela 6.4 se ejecuta antes que el QR 6.1.3). Las horas de cada actividad están en el documento de Estimación y Presupuesto (JJT-GPI-08).


### **1.0 Gestión del Proyecto** — Responsable: Tomás Disandro · Hito H1 · Sem. 1–5

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1.1 | Acta de Constitución | Tomás | Redacción y aprobación del acta que autoriza formalmente el proyecto: objetivos, alcance preliminar, sponsor, director de proyecto, hitos principales y criterios de éxito. Entregable: `docs/Acta Constitucion.md` aprobada por el sponsor. | — | Sem. 1 |
| 1.2 | Registro de Interesados | Tomás | Identificación de interesados internos (equipo, sponsor) y externos (usuarios del comercio, ARCA como organismo regulador, proveedor de infraestructura), y clasificación en matriz poder/interés para definir estrategia de comunicación con cada uno. | — | Sem. 1 |
| 1.3 | Documento de Requerimientos | Tomás | Relevamiento con el sponsor y redacción de los requerimientos funcionales (RF-01 a RF-32) y no funcionales (RNF-01 a RNF-10), con priorización (Alta/Media/Restricción), fuente y trazabilidad con los hitos H1–H4. | 1.1, 1.2 | Sem. 2 |
| 1.4 | Documento de Alcance y Gestión | Tomás | Declaración de alcance (in-scope / out-of-scope), elaboración de la EDT (9 paquetes de trabajo, `docs/EDT.md`), cronograma de hitos y sprints, y definición del proceso formal de control de cambios. | 1.3 | Sem. 2 |
| 1.5 | Revisión de pares de los documentos de gestión | Jesus | Revisión de pares (QA) de Acta, Interesados, Requerimientos, Alcance, EDT y Lista de Actividades: consistencia entre documentos, trazabilidad RF/RNF → EDT → hito y ortografía. Salida: lista de observaciones resueltas, requisito de la compuerta H1 (Plan de Calidad §7). | 1.4 | Sem. 2–5 |

### **2.0 Diseño y Arquitectura** — Responsable: Tomás Disandro · Hito H1 · Sem. 3–6

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 2.1 | Definición de stack tecnológico | Tomás | Selección de lenguaje/framework de backend y frontend, motor de base de datos, librería de firma y conexión SOAP a los Web Services de ARCA, y servicios de infraestructura (hosting, repositorio, CI/CD). | 1.4 | Sem. 3 |
| 2.2 | Modelo de datos genérico multirubro | Tomás | Diseño del esquema de datos parametrizable (RNF-01, RNF-02, RNF-03): categorías y atributos de variante definidos por el usuario en vez de columnas fijas, e IVA/tipos de comprobante configurables. Validado conceptualmente contra al menos 2 rubros (ej. kiosco e indumentaria) para anticipar el requisito de genericidad (RF-32). | 2.1 | Sem. 3–4 |
| 2.3 | Spike técnico homologación ARCA | Tomás | Prueba de concepto acotada de conexión a los Web Services de ARCA (WSAA/WSFEv1) contra el ambiente de homologación, usando certificado de testing sobre una CUIT de prueba, para des-riesgar tempranamente la integración antes de comprometer el desarrollo completo del módulo de Facturación (paquete 4.0, ruta crítica). | 2.1 | Sem. 4–6 |
| 2.4 | Revisión del modelo de datos contra 2 rubros | Jesus | Revisión independiente (QA) del modelo de datos de 2.2 contra dos rubros de ejemplo (kiosco e indumentaria): se verifica que categorías, variantes, IVA y tipos de comprobante se resuelvan por configuración y no por esquema. Anticipa RF-32 y mitiga el riesgo R8. | 2.2 | Sem. 4–6 |

### **3.0 Módulo Productos y Stock** — Responsable: Juan Cruz Bulatovich · Hito H2 · Sem. 7–15

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 3.1 | Alta/baja/modificación de productos | Juan | CRUD de productos del catálogo (código, descripción, precio, rubro/categoría) con validación de datos obligatorios, sobre el modelo de datos genérico definido en 2.2. Cubre RF-01. | 2.2, 2.3 | Sem. 7–8 |
| 3.2 | Categorías y variantes configurables | Juan | Definición de categorías por el usuario, sin categorías fijas de un rubro específico, y de atributos de variante (talle, color, presentación, etc.) mediante esquema configurable/extensible en lugar de columnas fijas en la base. Cubre RF-02, RF-03, RNF-02. | 3.1 | Sem. 10–11 |
| 3.3 | Control de inventario y ajustes | Juan | Registro del stock actual por producto/variante y funcionalidad de ajuste manual de stock con motivo obligatorio, para trazabilidad y auditoría de diferencias de inventario. Cubre RF-04. | 3.1 | Sem. 8–9 |
| 3.4 | Alertas de stock mínimo | Juan | Configuración de un umbral mínimo por producto/variante y generación de notificación visible cuando el stock actual cae por debajo de ese umbral. Cubre RF-05. | 3.3 | Sem. 9–10 |
| 3.5 | Pruebas funcionales de Productos y Stock | Jesus | Ejecución de las pruebas funcionales PC-STK (QA): CRUD, categorías y variantes configurables, ajuste con motivo y alerta de stock mínimo. Cubre la verificación de RF-01 a RF-05. | 3.4, 3.2 | Sem. 13–15 |

### **4.0 Módulo Facturación (ARCA)** — Responsable: Tomás Disandro · Hito H2 · Sem. 7–15 · Ruta crítica

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 4.1.1 | Autenticación WSAA | Tomás | Firma del Login Ticket Request (LTR) mediante CMS con el certificado de homologación/producción, envío al Web Service de Autenticación y Autorización, y obtención del Token/Sign de acceso. Base de RF-06 y RF-08. | 2.2, 2.3 | Sem. 7 |
| 4.1.2 | Cacheo y renovación del ticket | Tomás | Persistencia del Token/Sign obtenido junto a su fecha de expiración (~12 hs de vigencia) y lógica de renovación automática y transparente antes del vencimiento, evitando reautenticaciones innecesarias contra WSAA. | 4.1.1 | Sem. 7–8 |
| 4.1.3 | Cliente WSFEv1 | Tomás | Wrapper de conexión SOAP al servicio de Facturación Electrónica (WSFEv1) que reutiliza el Token/Sign cacheado para las operaciones de solicitud de CAE y consulta de comprobantes. | 4.1.2 | Sem. 8–9 |
| 4.2 | Emisión de Factura A/B/C | Tomás | Armado del comprobante según tipo (A, B o C) con datos de emisor/receptor, ítems e IVA discriminado; solicitud de CAE a ARCA vía WSFEv1 y persistencia del comprobante autorizado. Cubre RF-06. | 4.1.3 | Sem. 9–11 |
| 4.3 | Notas de Crédito/Débito | Tomás | Emisión de notas de crédito y débito asociadas a un comprobante previo, respetando la referencia al comprobante original y su impacto posterior en la cuenta corriente (paquete 5.0). Cubre RF-07. | 4.2 | Sem. 11–12 |
| 4.4 | Errores de WS y logging seguro | Tomás | Manejo explícito de rechazos y errores devueltos por ARCA —sin asumir que el CAE siempre se obtiene— y registro de logs de depuración que excluyan credenciales, certificados y datos sensibles. Cubre RF-09, RF-10, RNF-05. | 4.3 | Sem. 12–13 |
| 4.5 | Exportación de comprobantes PDF | Tomás | Generación de PDF imprimible del comprobante autorizado, con formato estándar: datos fiscales, detalle de ítems, IVA y CAE. Cubre RF-11. | 4.2 | Sem. 13–14 |
| 4.6 | Credenciales de producción | Tomás | Mecanismo configurable (variables de entorno) para alternar entre certificado de homologación (por defecto en desarrollo) y certificado de producción, sin hardcodear el ambiente ni commitear certificados/CUIT reales al repositorio. Cubre RF-08, RNF-04, RNF-09. | 4.4 | Sem. 14–15 |
| 4.7 | Pruebas de integración contra homologación ARCA | Jesus | Pruebas de integración PC-ARCA (QA con Tomás) contra homologación: Factura A/B/C, Notas de Crédito/Débito, error simulado de WS, revisión de logs sin credenciales y escaneo de secretos en el repositorio. Su cierre habilita la compuerta H2 (CE-1). | 4.3 | Sem. 12–15 |

### **5.0 Clientes/Proveedores y Cuentas Corrientes** — Responsable: Tomás Disandro · Hito H3 · Sem. 16–21

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 5.1 | ABM clientes/proveedores | Tomás | Alta, baja y modificación de clientes y proveedores con sus datos fiscales (CUIT/DNI, condición frente al IVA, domicilio), como base para asociar comprobantes (4.0) y pagos (6.0). Cubre RF-12. | 4.6 | Sem. 16–17 |
| 5.2 | Cuentas corrientes | Tomás | Registro de saldo por cliente/proveedor, historial de movimientos (débitos/créditos generados por ventas, pagos y notas de crédito/débito) y límite de crédito configurable con control al momento de superarlo. Cubre RF-13. | 5.1 | Sem. 17–18 |
| 5.3 | Consulta de estado de cuenta | Tomás | Vista de estado de cuenta corriente de un cliente/proveedor en un momento dado, con detalle de movimientos y saldo actual. Cubre RF-14. | 5.2 | Sem. 18–19 |
| 5.4 | Pruebas funcionales de Clientes/Proveedores | Jesus | Ejecución de las pruebas funcionales PC-CLI (QA): ABM con datos fiscales; saldo, movimientos y límite de crédito; estado de cuenta. Verifica RF-12 a RF-14. | 5.3 | Sem. 19–21 |

### **6.0 Módulo Pagos y Giftcards** — Responsable: Juan Cruz Bulatovich · Hito H3 · Sem. 16–21

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 6.1.1 | Efectivo y cuenta corriente | Juan | Registro de cobro en efectivo y de cobro imputado a la cuenta corriente del cliente (5.2), sin integración con servicios externos. Se programa después de 5.2 porque imputa sobre sus saldos y movimientos. Base de RF-15. | 5.2, 6.1.3 | Sem. 18 |
| 6.1.2 | Débito/crédito y transferencia | Juan | Registro del comprobante/referencia de pagos electrónicos (tarjeta de débito/crédito, transferencia bancaria) asociados a una venta. Base de RF-15. | 4.6 | Sem. 16 |
| 6.1.3 | QR | Juan | Flujo de cobro vía código QR contra la pasarela de pago simulada/sandbox (6.4), sin integrar pasarelas reales en esta entrega. Base de RF-15, alineado con la restricción RF-21. | 6.4 | Sem. 17 |
| 6.2 | Pago combinado / mixto | Juan | Combinación de más de un medio de pago en una misma venta, validando que la suma de los montos parciales cubra el total facturado. Cubre RF-16. | 6.1.1 | Sem. 18 |
| 6.3 | Giftcards | Juan | Ciclo completo de giftcards: emisión con código único, recarga de saldo, canje como medio de pago en una venta y consulta del saldo disponible. Cubre RF-17 a RF-20. | 6.2 | Sem. 18–19 |
| 6.4 | Pasarela simulada/sandbox | Juan | Construcción de la pasarela de pago simulada (sandbox) que emula respuestas de aprobación/rechazo y que consumen el flujo de QR (6.1.3) y, opcionalmente, el registro de tarjeta de 6.1.2; deja explícito que no se integran múltiples pasarelas reales en esta entrega. Cubre RF-21. | 6.1.2 | Sem. 16–17 |
| 6.5 | Pruebas funcionales de Pagos y Giftcards | Jesus | Ejecución de las pruebas funcionales PC-PAG (QA): cinco medios de pago, pago mixto, ciclo de giftcards y pasarela simulada. Verifica RF-15 a RF-21. | 6.3 | Sem. 19–21 |

### **7.0 Módulo Reportes y Estadísticas** — Responsable: Juan Cruz Bulatovich · Hito H3 · Sem. 19–23

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 7.1 | Ventas por período | Juan | Reporte de ventas filtrable por rango de fechas, con totales agregados y detalle por comprobante emitido (4.0) y por medio de pago (6.0). Cubre RF-22. | 5.3, 6.3 | Sem. 19–20 |
| 7.2 | Productos más vendidos | Juan | Ranking de productos/variantes ordenado por cantidad y/o monto vendido en el período seleccionado. Cubre RF-23. | 7.1 | Sem. 20 |
| 7.3 | Stock crítico | Juan | Listado de productos/variantes cuyo stock actual está por debajo del mínimo configurado en 3.4. Cubre RF-24. | 7.2 | Sem. 20–21 |
| 7.4 | Cuentas corrientes | Juan | Reporte consolidado del estado de cuentas corrientes de clientes y proveedores (5.2, 5.3). Cubre RF-25. | 7.3 | Sem. 21 |
| 7.5 | Rentabilidad | Juan | Reporte de margen entre costo y precio de venta por producto y/o período. Cubre RF-26. | 7.4 | Sem. 21–22 |
| 7.6 | Exportación de reportes | Juan | Exportación de los reportes de 7.1–7.5 a formatos PDF y/o CSV. Cubre RF-27. | 7.5 | Sem. 22 |
| 7.7 | Pruebas funcionales de Reportes | Jesus | Ejecución de las pruebas funcionales PC-REP (QA): cinco reportes y exportación, con conciliación contra ventas y comprobantes. Verifica RF-22 a RF-27. | 7.6 | Sem. 22–23 |

### **8.0 Módulo Usuarios y Permisos** — Responsable: Juan Cruz Bulatovich · Hito H3 · Sem. 22–23

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 8.1 | Rol administrador | Juan | Perfil con acceso a la configuración del sistema, gestión de usuarios y reportes completos (paquete 7.0), como rol base sobre el que se restringe el rol cajero. Hasta esta actividad los módulos operan con un usuario único provisorio de perfil administrador. Cubre RF-28, RF-29. | 7.6 | Sem. 22–23 |
| 8.2 | Rol cajero | Juan | Perfil con acceso limitado al flujo operativo de venta (stock, facturación, cobro), sin acceso a configuración sensible ni a gestión de usuarios. Cubre RF-28, RF-30. | 8.1 | Sem. 23 |
| 8.3 | Pruebas de permisos por rol | Jesus | Ejecución de las pruebas de permisos PC-USR (QA): administrador vs. cajero sobre cada módulo, incluido el acceso a configuración sensible. Verifica RF-28 a RF-30. | 8.2 | Sem. 23 |

### **9.0 Pruebas, Integración y Cierre** — Responsable: Jesus Manuel Martinez · Hito H4 · Sem. 24–27

| ID | Actividad | Responsable | Descripción | Predecesora | Duración |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 9.1 | Ciclo integral | Jesus | Prueba end-to-end del flujo completo: alta de producto → venta con control de stock → facturación (CAE) → registro de pago → impacto en reportes, verificando consistencia de datos entre todos los módulos. Incluye la inspección de la interfaz responsive en escritorio y móvil. Cubre RF-31 y RNF-06. | 8.2, 8.3, 7.7, 6.5 | Sem. 24–25 |
| 9.2 | Genericidad en ≥2 rubros | Jesus | Validación del modelo de datos configurando el sistema para 2 rubros comerciales distintos (ej. kiosco y tienda de indumentaria) usando solo configuración/datos, sin cambios de código. Cubre RF-32. | 9.1 | Sem. 25–26 |
| 9.3 | Validación final ARCA | Jesus | Validación final de emisión de comprobantes contra el ambiente de homologación de ARCA, confirmando obtención de CAE en los escenarios probados (Factura A/B/C, Notas de Crédito/Débito). Cubre CE-1. | 9.2 | Sem. 26 |
| 9.4 | Entrega final y cierre | Jesus | Entrega del sistema al sponsor junto con la documentación de cierre del proyecto (estado final de alcance, lecciones aprendidas). Verifica que lo excluido no se implementó (RNF-07), que los cambios pasaron por el control de cambios (RNF-08) y que el equipo se mantuvo fijo (RNF-10). | 9.3 | Sem. 27 |

---

**Total: 48 actividades** repartidas en 9 paquetes de trabajo (EDT §1.0–9.0): 40 originales y 8 de aseguramiento de calidad por módulo.
