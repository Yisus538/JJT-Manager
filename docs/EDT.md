JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Estructura de Desglose del Trabajo (EDT)**

Sistema de Gestión y Facturación Ágil integrado con ARCA

Sponsor **Julio Gutierrez** · Director de proyecto **Tomás Disandro**

**Leyenda de responsables:** 🔵 Tomás — Backend / PM · 🟠 Juan — Frontend · 🟢 Jesus — QA y QC

## JJT Manager

Sistema de Gestión y Facturación Ágil integrado con ARCA

---

## 1.0 Gestión del Proyecto `H1` 🔵 Tomás

Documentación de gestión: acta, interesados, requerimientos y alcance.

* **1.1** Acta de Constitución
* **1.2** Registro de Interesados
* **1.3** Documento de Requerimientos
* **1.4** Documento de Alcance y Gestión

## 2.0 Diseño y Arquitectura `H1` 🔵 Tomás

Definición técnica del sistema y validación temprana del riesgo ARCA.

* **2.1** Definición de stack tecnológico
* **2.2** Modelo de datos genérico multirubro — `RNF-01–03`
* **2.3** Spike técnico homologación ARCA

## 3.0 Módulo Productos y Stock `H2` 🟠 Juan

Catálogo, categorías, variantes e inventario configurables por rubro.

* **3.1** Alta/baja/modificación de productos — `RF-01`
* **3.2** Categorías y variantes configurables — `RF-02, 03`
* **3.3** Control de inventario y ajustes — `RF-04`
* **3.4** Alertas de stock mínimo — `RF-05`

## 4.0 Módulo Facturación (ARCA) `H2` 🔵 Tomás — Ruta crítica

Emisión de comprobantes electrónicos válidos ante ARCA.

* **4.1** Integración WSAA/WSFEv1 — homologación — `RF-06, 08`
  * **4.1.1** Autenticación WSAA: firma del Login Ticket Request y obtención de Token/Sign
  * **4.1.2** Cacheo y renovación automática del ticket de acceso (~12 hs de vigencia)
  * **4.1.3** Cliente WSFEv1: wrapper de conexión al servicio de facturación electrónica
* **4.2** Emisión de Factura A/B/C — `RF-06`
* **4.3** Notas de Crédito/Débito — `RF-07`
* **4.4** Errores de WS y logging seguro — `RF-09, 10`
* **4.5** Exportación de comprobantes PDF — `RF-11`
* **4.6** Credenciales de producción — `RF-08`

## 5.0 Clientes/Proveedores y Cuentas Corrientes `H3` 🔵 Tomás

Datos fiscales y cuentas corrientes de clientes y proveedores.

* **5.1** ABM clientes/proveedores con datos fiscales — `RF-12`
* **5.2** Cuentas corrientes: saldo, movimientos, límite — `RF-13`
* **5.3** Consulta de estado de cuenta — `RF-14`

## 6.0 Módulo Pagos y Giftcards `H3` 🟠 Juan

Cobro con medios combinables y ciclo completo de giftcards.

* **6.1** Medios de pago múltiples — `RF-15`
  * **6.1.1** Efectivo y cuenta corriente (sin integración externa)
  * **6.1.2** Débito/crédito y transferencia (registro de comprobante)
  * **6.1.3** QR — flujo de cobro contra la pasarela simulada
* **6.2** Pago combinado / mixto — `RF-16`
* **6.3** Giftcards: emisión, recarga, canje — `RF-17–20`
* **6.4** Pasarela simulada/sandbox — `RF-21`

## 7.0 Módulo Reportes y Estadísticas `H3` 🟠 Juan

Métricas de ventas, stock, cuentas y rentabilidad, exportables.

* **7.1** Ventas por período — `RF-22`
* **7.2** Productos más vendidos — `RF-23`
* **7.3** Stock crítico — `RF-24`
* **7.4** Cuentas corrientes — `RF-25`
* **7.5** Rentabilidad — `RF-26`
* **7.6** Exportación de reportes — `RF-27`

## 8.0 Módulo Usuarios y Permisos `H3` 🟠 Juan

Roles administrador y cajero con permisos diferenciados.

* **8.1** Rol administrador — `RF-29`
* **8.2** Rol cajero — `RF-30`

## 9.0 Pruebas, Integración y Cierre `H4` 🟢 Jesus

Validación end-to-end del sistema y entrega final del proyecto.

* **9.1** Ciclo integral: alta → venta → facturación → pago → reportes — `RF-31`
* **9.2** Genericidad en ≥2 rubros — `RF-32`
* **9.3** Validación final homologación ARCA
* **9.4** Entrega final y documentación de cierre

---

JJT Manager — Estructura de Desglose del Trabajo
