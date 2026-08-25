# Deuda Técnica — JJT Manager

**Última actualización:** 2026-08-25 — sin ítems registrados todavía (proyecto en fase de documentación, sin código desarrollado aún).

> Los ítems ya resueltos se mueven a `TECH_DEBT_RESUELTO.md`.
> Las auditorías de código (cuando existan) van en `qa/audits/`.
> Quién resuelve cada ítem: ver la sección "Deuda técnica: quién la resuelve" en `CLAUDE.md` de esta carpeta.

---

## Convención

- **ID:** `TD-XXX`, correlativo, nunca se reutiliza aunque el ítem se cierre por obsolescencia en vez de por fix.
- **Severidad:** Alta / Media / Baja — según impacto real en el usuario final o en el equipo, no según cuánto cueste arreglarlo.
- **Módulo:** `Frontend` | `Backend` | `Cross` (afecta el contrato entre ambos, ej. forma de la API).
- Cada ítem lleva estos campos:
  - **Archivos afectados**
  - **Descripción** — qué se encontró y cómo (auditoría, testing manual, revisión de código, etc.)
  - **Riesgo** — qué pasa si no se arregla
  - **Recomendación** — qué hacer, y de quién depende
- El encabezado (`Última actualización`) es un changelog corto: qué se resolvió, qué es nuevo, con referencia al TD-XXX correspondiente. Mantenerlo actualizado en cada sesión de testing, no solo cuando se cierra un ítem.

---

## Alta

_Sin ítems registrados._

## Media

_Sin ítems registrados._

## Baja

_Sin ítems registrados._
