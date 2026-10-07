JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Revisión del Modelo de Datos contra Dos Rubros**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-16 |
| Actividad | 2.4 Revisión del modelo de datos contra 2 rubros (Lista de Actividades v1.2) |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Revisor | Jesus Manuel Martinez (QA y QC) |
| Fecha / Versión / Estado | 07/10/2026 · 1.0 · Completada · aprobada por el equipo |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 07/10/2026 | Emisión inicial: revisión del Modelo de Datos v1.0 y cierre con la v1.1. Emitido fuera del plazo previsto (semanas 4–6). |

> Revisión de QA del Modelo de Datos Genérico (JJT-GPI-15) contra los dos rubros de ejemplo (kiosco e indumentaria): se verifica que categorías, variantes, IVA y tipos de comprobante se resuelvan **por configuración y no por esquema** (Plan de Calidad §3; riesgo R8; criterio CE-3). Esta revisión es documental: recorre escenarios de uso contra el modelo; la verificación con datos reales se hace en las pruebas 3.5, 9.2 y 9.1.

## **1. Método**

1. Se definieron seis escenarios por rubro a partir de las operaciones diarias de cada comercio.
2. Para cada escenario se identificó qué entidades y campos del modelo v1.0 lo resuelven y si hace falta **un cambio de estructura o solo carga de datos**.
3. Cada brecha se registró como observación, se resolvió en el modelo (v1.1) y se volvió a verificar el escenario.
4. Criterio de aprobación: ningún escenario de los dos rubros exige agregar tablas, columnas ni lógica específica de un rubro.

## **2. Escenarios y resultado sobre el modelo v1.0**

| N.º | Rubro | Escenario | Resolución en el modelo | Resultado v1.0 |
| :----: | :---- | :---- | :---- | :---- |
| K1 | Kiosco | Venta de un alfajor, 1 unidad, con IVA 21 % incluido en el precio | `producto` + variante única; precio base; `alicuota_iva` | Brecha (O5) |
| K2 | Kiosco | Venta de 0,350 kg de fiambre a granel | `venta_item.cantidad` | Brecha (O1) |
| K3 | Kiosco | Gaseosa en tres presentaciones (500 ml, 1,5 L, 2,25 L) | `atributo_def` «Presentación» y tres variantes | Cumple |
| K4 | Kiosco | Venta a consumidor final sin datos, pago con efectivo y QR | `venta.tercero_id`, `pago` ×2 | Brecha (O3) |
| K5 | Kiosco | Fiado a un vecino con límite de crédito y cobro posterior | `tercero`, `cuenta_corriente`, `movimiento_cc` | Cumple |
| K6 | Kiosco | Alerta de stock mínimo de golosinas de alta rotación | `variante.stock_minimo` | Cumple |
| I1 | Indumentaria | Remera en 4 talles × 3 colores | `atributo_def` «Talle» y «Color», 12 variantes | Cumple |
| I2 | Indumentaria | Talle XXL con precio mayor que el resto | Precio por variante | Brecha (O2) |
| I3 | Indumentaria | Cambio de prenda: nota de crédito y nueva venta | `comprobante_asociado_id`, `movimiento_stock` de devolución | Cumple |
| I4 | Indumentaria | Venta con tarjeta y giftcard (pago mixto) | `pago` ×2, `giftcard`, `movimiento_giftcard` | Cumple |
| I5 | Indumentaria | Emisor monotributista: debe emitir Factura C | `tipo_comprobante` y condición de IVA del emisor | Brecha (O4) |
| I6 | Indumentaria | Ajuste de stock por prenda dañada con motivo | `movimiento_stock` con motivo obligatorio | Cumple |

## **3. Observaciones y resolución**

| N.º | Observación | Escenario | Gravedad | Resolución (Modelo de Datos v1.1) | Estado |
| :----: | :---- | :---- | :----: | :---- | :---- |
| O1 | El modelo v1.0 no distinguía cantidades decimales ni unidad de medida, necesarias para ventas a granel (peso, volumen). | K2 | Alta | `producto.unidad_medida` y cantidades `NUMERIC(12,3)` en `venta_item` y `movimiento_stock`. | Resuelta |
| O2 | El precio estaba solo en el producto; una variante no podía tener un precio distinto. | I2 | Media | `variante.precio_propio` y `variante.precio_venta`; si no hay precio propio rige `producto.precio_base`. | Resuelta |
| O3 | Toda venta exigía un cliente; no cubría el consumidor final sin identificar. | K4 | Alta | `venta.tercero_id` admite nulo (consumidor final); el comprobante informa «sin identificar» según `tipo_comprobante.requiere_receptor_identificado`. | Resuelta |
| O4 | No había forma de decidir si el emisor emite Factura A/B o C. | I5 | Alta | `comercio.condicion_iva_emisor` y regla de integridad 10 (tipos permitidos por condición de IVA). | Resuelta |
| O5 | No estaba definido si los precios incluyen IVA; en comercio minorista el precio de góndola es el precio final. | K1 | Media | `comercio.precios_incluyen_iva`; el servicio desglosa el IVA al emitir. | Resuelta |

Todas las brechas se resolvieron con **campos y datos de configuración genéricos**; ninguna con estructura específica de un rubro.

## **4. Verificación de los requisitos de genericidad**

| Requisito | Verificación | Resultado |
| :---- | :---- | :---- |
| RNF-01 No asumir un rubro | No hay tablas ni columnas con nombres de rubro; las categorías y los atributos son filas. | Cumple |
| RNF-02 Atributos configurables | `atributo_def` + `variante.atributos` (JSONB validado). Un rubro nuevo agrega filas, no columnas. | Cumple |
| RNF-03 IVA y comprobantes parametrizables | `alicuota_iva` y `tipo_comprobante` con códigos de ARCA como datos. | Cumple |
| RF-32 / CE-3 Dos rubros sin cambios de código | Los dos rubros se cargan solo con datos (Modelo de Datos §5). | Cumple en diseño; **se confirma en las pruebas 9.2** |

## **5. Riesgos residuales y recomendaciones para las pruebas**

| N.º | Riesgo residual | Recomendación |
| :----: | :---- | :---- |
| 1 | Un atributo con `JSONB` pierde las garantías de tipo de las columnas. | Pruebas de validación de atributos contra `atributo_def` en 3.5 (PC-STK); índices `GIN` si se filtra por atributo. |
| 2 | Denormalización de saldos (`stock_actual`, `saldo`): puede desfasarse de los movimientos. | Pruebas de conciliación en 3.5, 5.4 y 6.5 (suma de movimientos = saldo). |
| 3 | Los rubros con otras necesidades (vencimientos, números de serie, recetas) no están cubiertos. | Fuera del alcance de esta entrega; se tratan por control de cambios (Alcance §7) si se piden. |
| 4 | La revisión es documental y la realizó una sola persona de QA. | La verificación con datos reales de ambos rubros se repite en 9.2 antes del cierre de H4. |

## **6. Conclusión**

El modelo, en su versión 1.1, resuelve los doce escenarios de los dos rubros **sin cambios de estructura**, solo con carga de datos. La actividad **2.4 queda completada** y reduce la exposición del riesgo R8, que se mantiene en monitoreo hasta la prueba 9.2.

## **7. Aprobación**

*Aprobado por el equipo el 07/10/2026. Firma y fecha de cada persona, a registrar en la tabla.*

| Rol | Nombre | Firma / Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Revisor (QA y QC) | Jesus Manuel Martinez | | |
| Director de proyecto y Backend | Tomás Disandro | | |
| Frontend | Juan Cruz Bulatovich | | |
