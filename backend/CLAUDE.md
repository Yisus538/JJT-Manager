# backend/ — JJT Manager

Dueño: **Tomás Disandro** (Backend / Director de Proyecto).

## Alcance

Esta carpeta es del integrante de Backend. Contiene la API, el modelo de datos genérico multirubro, la integración con los Web Services de ARCA (facturación electrónica), y la lógica de negocio de stock, clientes/proveedores, cuentas corrientes, pagos y giftcards.

## Reglas para agentes de IA

- No edites ni escribas archivos en `../frontend/`. Si necesitás un cambio de UI o de cómo se consume la API, documentalo (en `../docs/`) y coordiná con el dueño de `frontend/`.
- No edites archivos en `../qa/` salvo que Jesus (QA/QC) lo pida explícitamente.
- Podés leer `../docs/` libremente para contexto de requisitos/alcance, y escribir ahí documentación relacionada a backend si corresponde (ej. definición de endpoints, modelo de datos).
- Excepción conocida: Jesus Manuel Martinez (QA y QC) puede leer y escribir en esta carpeta como parte de testing — eso es esperado, no es una violación de ownership.

## Deuda técnica

La deuda técnica de severidad **Alta y Media** de este módulo se registra en `docs/TECH_DEBT.md` (histórico de resueltos en `docs/TECH_DEBT_RESUELTO.md`) y es responsabilidad de Tomás Disandro resolverla. Deuda de severidad **Baja** que encuentre QA/QC en este módulo la resuelve QA/QC directo y queda anotada en `../qa/TECH_DEBT.md`, no acá.
