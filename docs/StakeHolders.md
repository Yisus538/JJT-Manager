

DOCUMENTO DE  GESTIÓN  DE  PROYECTOS

# **Registro de Interesados**

Sistema de Gestión y Facturación Ágil integrado con ARCA 

Nombre corto del proyecto	**JJT Manager**

Patrocinador (Sponsor)	**Julio Gutierrez**

Director de proyecto	**Tomas Disandro**

Fecha	**25/08/2026**

## **Registro de Interesados (Stakeholder Register)**

**Proyecto:** Sistema de Gestión y Facturación Ágil integrado con ARCA (JJT Manager)

**Fecha:** 25/08/2026 

1. ### **Metodología de clasificación**

Se utiliza la **matriz Poder/Interés**, estándar en PMBOK, con cuatro cuadrantes y estrategia de involucramiento asociada:

| Cuadrante | Poder | Interés | Estrategia |
| :---- | :---- | :---- | :---- |
| A | Alto | Alto | **Gestionar de cerca** (Manage Closely) — involucramiento activo, comunicación frecuente y directa. |
| B | Alto | Bajo | **Mantener satisfecho** (Keep Satisfied) — informar lo suficiente para evitar fricción, sin sobrecargar. |
| C | Bajo | Alto | **Mantener informado** (Keep Informed) — comunicación regular, se busca su feedback pero no decide. |
| D | Bajo | Bajo | **Monitorear** (Monitor) — esfuerzo mínimo de comunicación, seguimiento pasivo. |

**Poder** \= capacidad de influir en decisiones de alcance, cronograma o presupuesto del proyecto.

**Interés** \= grado en que el resultado del proyecto afecta o preocupa al interesado.

2. ### **Registro de interesados**

Cada interesado se documenta con una ficha Campo/Detalle, en el mismo formato usado por el Acta de Constitución (sección "Datos generales").

#### **STK-01 — Julio Gutierrez**

| Rol / Interés | Sponsor / Cliente. Financia y valida el proyecto a alto nivel. |
| :---- | :---- |
| **Poder** | Alto |
| **Interés** | Alto |
| **Cuadrante** | A |
| **Estrategia** | Gestionar de cerca |
| **Fuente (trazabilidad)** | Acta "Datos generales" (Patrocinador); "Interesados (Stakeholders) principales"; "Aprobación" |

#### **STK-02 — Tomas Disandro**

| Rol / Interés | Director de Proyecto y Backend. Autoridad para asignar tareas, priorizar backlog, proponer cambios de alcance y representar al equipo ante el sponsor. |
| :---- | :---- |
| **Poder** | Alto |
| **Interés** | Alto |
| **Cuadrante** | A |
| **Estrategia** | Gestionar de cerca |
| **Fuente (trazabilidad)** | Acta "Datos generales" (Director de proyecto / Equipo); "Autoridad del Director de Proyecto" |

#### **STK-03 — Juan Cruz Bulatovich**

| Rol / Interés | Integrante del equipo — Frontend. Ejecutor directo del desarrollo. |
| :---- | :---- |
| **Poder** | Medio |
| **Interés** | Alto |
| **Cuadrante** | A (límite con C) |
| **Estrategia** | Gestionar de cerca |
| **Fuente (trazabilidad)** | Acta "Datos generales" (Equipo del proyecto); "Interesados (Stakeholders) principales" ("Ejecutores: desarrollo, gestión y documentación") |

#### **STK-04 — Jesus Manuel Martinez**

| Rol / Interés | Integrante del equipo — QA y QC. Responsable de validar la calidad del producto. |
| :---- | :---- |
| **Poder** | Medio |
| **Interés** | Alto |
| **Cuadrante** | A (límite con C) |
| **Estrategia** | Gestionar de cerca |
| **Fuente (trazabilidad)** | Acta "Datos generales" (Equipo del proyecto); "Interesados (Stakeholders) principales" |

#### **STK-05 — Comerciante tipo kiosco/tienda indumentaria (genérico)**

| Rol / Interés | Usuario objetivo final; valida usabilidad y utilidad del sistema para su rubro. Valida que el modelo de datos sea genérico y no esté atado a un solo tipo de comercio. |
| :---- | :---- |
| **Poder** | Bajo |
| **Interés** | Alto |
| **Cuadrante** | C |
| **Estrategia** | Mantener informado |
| **Fuente (trazabilidad)** | Acta "Interesados (Stakeholders) principales" ("Comerciante/usuario final... valida usabilidad y utilidad"); "Criterios de éxito" (aplicable a ≥2 rubros, ej. kiosco,indumentaria) |

#### **STK-06 — ARCA (organismo fiscal)**

| Rol / Interés | Define las reglas y Web Services (WSAA/WSFEv1) con los que el sistema debe interoperar para emitir comprobantes válidos. No participa activamente del proyecto pero sus reglas condicionan el desarrollo. |
| :---- | :---- |
| **Poder** | Alto |
| **Interés** | Bajo |
| **Cuadrante** | B |
| **Estrategia** | Mantener satisfecho |
| **Fuente (trazabilidad)** | Acta "Interesados (Stakeholders) principales"; "Objetivos específicos" (integración con WS de ARCA); "Restricciones y supuestos"; "Riesgos de alto nivel identificados" (complejidad de WS de ARCA) |

#### **STK-07 — Proveedor de infraestructura (Railway)**

| Rol / Interés | Provee el hosting/servidor sobre el que corre el sistema. Interesado técnico externo, sin influencia sobre decisiones de producto. |
| :---- | :---- |
| **Poder** | Bajo |
| **Interés** | Bajo |
| **Cuadrante** | D |
| **Estrategia** | Monitorear |
| **Fuente (trazabilidad)** | Acta "Presupuesto de alto nivel" (Costos de Infraestructura: Railway, 5 USD/mes) |

3. ### **Matriz Poder/Interés (visual)**

| Poder \\ Interés | Bajo | Alto |
| :---- | :---- | :---- |
| **Alto** | STK-06 (ARCA) | STK-01 (Sponsor), STK-02 (Director), STK-03 (Frontend), STK-04 (QA/QC) |
| **Bajo** | STK-07 (Railway) | STK-05 (Comerciante genérico) |

4. ### **Notas de trazabilidad y decisiones de alcance de este registro**

   * **STK-03 y STK-04** quedan en el límite entre cuadrante A y C: tienen poder de decisión técnica dentro de su rol, pero no autoridad formal de priorización de alcance (esa autoridad es exclusiva de STK-02 según "Autoridad del Director de Proyecto"). Se los clasificó en A por ser ejecutores directos con voz en decisiones técnicas cotidianas.

   * **STK-06 (ARCA)** se mantiene como una única entrada (no se separó en "ARCA regulador" vs "ARCA como proveedor técnico de WS") por decisión explícita: es la misma entidad y separarla generaría redundancia sin aportar trazabilidad adicional.

