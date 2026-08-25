# JJT Manager — Sistema de Gestión y Facturación Ágil integrado con ARCA

Monorepo del proyecto de la materia Gestión de Proyectos Informáticos. Ver `docs/Acta Constitucion.md` para el detalle completo del proyecto.

## Equipo y ownership de carpetas

| Carpeta | Dueño/a | Rol |
|---|---|---|
| `frontend/` | Juan Cruz Bulatovich | Frontend |
| `backend/` | Tomás Disandro | Backend / Director de Proyecto |
| `qa/` | Jesus Manuel Martinez | QA y QC |
| `docs/` | Compartida | Todo el equipo |

## Regla de ownership (para cualquier agente de IA que trabaje en este repo)

- **No edites ni escribas archivos fuera de la carpeta de tu dueño/a**, salvo `docs/` que es compartida.
- Cada carpeta (`frontend/`, `backend/`, `qa/`) tiene su propio `CLAUDE.md` con el detalle de su alcance. Leelo antes de trabajar ahí.
- Excepción: **QA y QC** (Jesus Manuel Martinez) puede leer y escribir tanto en `frontend/` como en `backend/`, además de `qa/`, porque su rol implica testing cruzado, reporte de bugs y validación end-to-end sobre ambos módulos.
- Si tu tarea requiere un cambio en una carpeta que no es la tuya, no lo hagas directamente: documentalo (en `docs/` o como issue) y notificá al dueño/a de esa carpeta.
- `docs/` es de escritura compartida: cualquiera puede agregar/actualizar documentación de gestión ahí.

## Cómo trabajar cada integrante

Cada integrante debe abrir Claude Code con working directory dentro de su propia carpeta (`cd frontend && claude`, `cd backend && claude`, `cd qa && claude`). Esto limita por defecto el acceso a archivos fuera de esa carpeta.

Además, cada carpeta trae un `.claude/settings.local.json.example` con reglas de permisos (`allow`/`deny`) que refuerzan esta separación. **Al clonar el repo, cada integrante debe copiar el suyo:**

```bash
# Juan (frontend)
cp frontend/.claude/settings.local.json.example frontend/.claude/settings.local.json

# Tomás (backend)
cp backend/.claude/settings.local.json.example backend/.claude/settings.local.json

# Jesus (qa)
cp qa/.claude/settings.local.json.example qa/.claude/settings.local.json
```

`settings.local.json` (sin `.example`) está en `.gitignore` — es personal de cada máquina, no se sube al repo.

## Convención de commits (a definir cuando se cree el repo Git)

Sugerido: `[frontend|backend|qa|docs] descripción breve`, para que quede claro a qué carpeta pertenece cada cambio y facilitar la revisión cruzada.
