# Deuda Técnica — QA/QC (severidad Baja)

**Última actualización:** 2026-08-25 — sin ítems registrados todavía (proyecto en fase de documentación, sin código desarrollado aún).

> Este archivo es solo para deuda de **severidad Baja** — la que QA/QC detecta y resuelve directamente (ver regla en `CLAUDE.md` de esta carpeta).
> Deuda **Alta** y **Media** se registra en el `docs/TECH_DEBT.md` del módulo dueño: `frontend/docs/TECH_DEBT.md` o `backend/docs/TECH_DEBT.md`.
> Los ítems ya resueltos se mueven a `TECH_DEBT_RESUELTO.md`.

---

## Convención

- **ID:** `TD-XXX`, correlativo, nunca se reutiliza aunque el ítem se cierre por obsolescencia en vez de por fix.
- **Módulo:** `Frontend` | `Backend` (dónde está el archivo afectado, aunque el fix lo haga QA/QC).
- Cada ítem lleva estos campos:
  - **Archivos afectados**
  - **Descripción** — qué se encontró y cómo (testing manual, E2E, revisión de código, etc.)
  - **Riesgo** — por qué se clasifica como Baja y no como Media/Alta
  - **Recomendación** — qué se hizo o qué falta hacer
- Si al investigar un ítem Baja aparece algo que en realidad es Media o Alta, no se anota acá: se migra al `TECH_DEBT.md` del módulo correspondiente y se anota quién lo asumió.
- El encabezado (`Última actualización`) es un changelog corto: qué se resolvió, qué es nuevo, con referencia al TD-XXX correspondiente. Mantenerlo actualizado en cada sesión de testing.

---

## Baja

_Sin ítems registrados._
