# CONTEXTO-PROYECTO.md — DevBrain

> Este archivo es la memoria del proyecto. Actualízalo al final de cada sprint o cuando algo importante cambie. Pégalo al inicio de cualquier conversación nueva con Claude para continuar sin perder contexto.

---

## 1. Descripción del proyecto

**DevBrain** es una plataforma web para la gestión del conocimiento técnico dentro de proyectos de software. Permite registrar, organizar y consultar decisiones técnicas importantes, respondiendo preguntas como: ¿por qué se migró de MySQL a PostgreSQL? ¿Quién propuso esta arquitectura? ¿Qué alternativas se evaluaron?

**Materia:** Administración de Proyectos para TI
**Universidad:** Universidad Tecnológica de Puebla
**Fecha de entrega:** 14 de julio de 2026
**Sprint actual:** Sprint 3 (2-8 jul 2026)

---

## 2. Equipo

| Nombre | Usuario GitHub | Rol principal |
|---|---|---|
| Joseph | Joseph-VZ | Líder del proyecto, gestión e integración final |
| Jesús | JessAckerman | Responsable Frontend (Vue 3) |
| Vanessa | VKrystal- | Responsable Base de datos (Supabase/PostgreSQL) |
| América | ame-97 | Responsable API Backend (Node.js/Express) |
| Adolfo | ZAYASNVP | Responsable QA + apoyo Frontend |

Todos tienen acceso a los 3 repositorios.

---

## 3. Stack tecnológico

| Capa | Tecnología | Despliegue |
|---|---|---|
| Frontend | Vue 3, Pinia, Vue Router, Tailwind CSS | Vercel |
| Backend | Node.js, Express, TypeScript | Render |
| Base de datos | PostgreSQL | Supabase |
| Autenticación | JWT | — |
| IA | Gemini API | — |

---

## 4. Repositorios

| Repo | URL | Contenido |
|---|---|---|
| DevBrain-Frontend | github.com/Joseph-VZ/DevBrain-Frontend | Código Vue 3 |
| DevBrain-Backend | github.com/Joseph-VZ/DevBrain-BackEnd | Código Node.js/Express |
| DevBrain-ProjectManagement | github.com/Joseph-VZ/DevBrain-ProjectManagement | Documentación y gestión |

**Reglas de ramas:**
- `main` — código estable, solo se actualiza al cerrar un sprint (Joseph abre el PR develop → main)
- `develop` — integración diaria del equipo (1 aprobación requerida)
- Todo trabajo en ramas `feature/`, `fix/` o `docs/` y entra por Pull Request hacia develop
- Nadie hace push directo a `main` ni a `develop`
- Nombre de ramas: `feature/<numero-issue>-descripcion-corta`

**Problema recurrente en Sprint 2:** varios PRs fueron mergeados a `main` en lugar de `develop`. Se sincronizaron manualmente. Reforzar esta regla en Sprint 3.

---

## 5. Estructura de carpetas

### DevBrain-ProjectManagement
```
00-actas/          → kickoff, sprint reviews
01-requerimientos/ → RF, RNF, contexto del problema
02-casos-de-uso/   → diagramas UML
03-arquitectura/   → diagrama arquitectura, E-R, API_CONTRACT.md
04-planeacion/     → gantt, guía de despliegue
05-riesgos/        → matriz de riesgos
06-sprint-backlog/ → backlog por sprint
07-minutas/        → minutas de sprint reviews
08-evidencias/     → capturas por sprint
09-pruebas/        → plan y resultados de pruebas
10-lecciones-aprendidas/
11-documentacion-final/
```

### DevBrain-Backend
```
src/config/        → conexión BD, variables de entorno
src/controllers/   → authController, projectController, decisionController, voteController, aiController
src/middleware/    → auth.middleware.ts (JWT)
src/models/        → queries SQL directas (sin ORM)
src/routes/        → rutas por módulo
src/services/      → aiService, authService
db/                → schema.sql
```

**Nota:** Existen archivos duplicados detectados en Sprint 2: `projectController.ts` / `projectsController.ts` y `project.routes.ts` / `projects.routes.ts`. América y Vanessa deben identificar y eliminar los sobrantes.

### DevBrain-Frontend
```
src/components/    → common, decisions, projects, timeline, ai
src/views/         → auth, dashboard, projects, decisions, ai
src/stores/        → auth.js, projects.js, decisions.js, ui.js
src/router/        → index.js
src/services/      → api.js (Axios), authService, projectService, decisionService, aiService
```

---

## 6. MVP obligatorio

- Login y registro ✅ (Sprint 2)
- Gestión de proyectos (CRUD) ✅ (Sprint 2)
- Registro de decisiones técnicas (con contexto y alternativas) ⏳ Sprint 3
- Sistema de votación (a favor / en contra) ⏳ Sprint 3
- Timeline cronológico de decisiones ⏳ Sprint 3
- Consulta mediante IA (Gemini) con contexto real del proyecto ⏳ Sprint 3
- API REST documentada ⏳ Sprint 3
- Despliegue funcional ⏳ Sprint 4

---

## 7. Estado del proyecto

### Sprint 1 — Completado ✅ (18-24 jun)
- 18 de 19 issues completados
- Estructura de los 3 repos, GitHub Project, documentación base completa

### Sprint 2 — Completado ✅ (25 jun – 4 jul, extendido por correcciones)
- Login y gestión de proyectos funcionales en frontend y backend
- Base de datos desplegada en Supabase
- Problemas encontrados y corregidos:
  - PRs de América y Jesús mergeados a main en lugar de develop (sincronizados manualmente)
  - Archivos duplicados en Backend (pendiente de limpieza por América/Vanessa)
  - Nombres de ramas no siguieron la convención acordada

### Sprint 3 — En curso ⏳ (2-8 jul)

| Código | Título | Asignado | Repo | Estado |
|---|---|---|---|---|
| BACK-07 | Endpoints CRUD de decisiones | Vanessa | Backend | ⏳ |
| BACK-08 | Endpoint de votación | Vanessa | Backend | ⏳ |
| BACK-09 | Integrar Gemini API (/ai/query) | América | Backend | ⏳ |
| BACK-10 | Documentar endpoints decisiones/votación/IA | América + Joseph | ProjectManagement | ⏳ |
| FRONT-07 | Vista de registro de decisiones | Jesús | Frontend | ⏳ |
| FRONT-08 | Vista de votación | Jesús | Frontend | ⏳ |
| FRONT-09 | Vista de timeline cronológico | Jesús | Frontend | ⏳ |
| FRONT-10 | Vista de consulta IA | Adolfo | Frontend | ⏳ |
| FRONT-11 | Pruebas de decisiones, votación y timeline | Adolfo | Frontend | ⏳ |
| FRONT-12 | Pruebas de integración frontend-backend | Adolfo | Frontend | ⏳ |
| PM-03 | Minuta Sprint 2 Review + backlog Sprint 3 | Joseph | ProjectManagement | ⏳ |
| PM-04 | ~~Actualizar API_CONTRACT.md~~ | — | — | ❌ Fusionado con BACK-10 |

**Dependencias clave Sprint 3:**
- BACK-07 y BACK-08 deben estar listos antes de que Jesús empiece FRONT-07, FRONT-08 y FRONT-09
- BACK-09 debe estar listo antes de que Adolfo empiece FRONT-10 y FRONT-12
- ⚠️ BACK-09 requiere que GEMINI_API_KEY esté configurada en .env antes de empezar

---

## 8. Decisiones técnicas tomadas

| Decisión | Razón |
|---|---|
| TypeScript en backend, JavaScript en frontend | TS da tipado en la API donde los errores de tipo cuestan más |
| Sin ORM (queries SQL directas con `pg`) | Menos configuración, errores más claros |
| Gemini no accede directo a la BD | El backend construye el contexto desde PostgreSQL y lo pasa al prompt |
| 3 repositorios separados | Frontend, Backend y Gestión separados por naturaleza del contenido |
| Vanessa = Base de datos, América = API | Cada persona documenta su propio trabajo |
| Adolfo apoya en código frontend además de QA | Mayor equidad en carga de trabajo |

---

## 9. Convenciones de commits

```
feat:     nueva funcionalidad
fix:      corrección de bug
docs:     documentación
chore:    configuración, setup
test:     pruebas
refactor: refactorización sin cambio funcional
```

Ejemplo: `feat(auth): add JWT middleware validation`

---

## 10. GitHub Project

- **Tablero:** DevBrain - Gestión General (en DevBrain-ProjectManagement)
- **Columnas:** 📋 Backlog / 🔜 Sprint Actual / 🔄 En Progreso / 👀 En Revisión / ✅ Completado / 🚫 Bloqueado
- **Milestones:** Sprint 1 al 4 + Entrega Final (en los 3 repos)
- **Labels:** 18 labels en los 3 repos (type, priority, scope, status, sprint)

---

## 11. Pendientes inmediatos

1. **América/Vanessa** — eliminar archivos duplicados en Backend (projectsController.ts y projects.routes.ts)
2. **Todo el equipo** — respetar la regla de PRs hacia `develop`, no hacia `main`
3. **América** — configurar GEMINI_API_KEY en .env antes de empezar BACK-09
4. **Joseph** — redactar minuta Sprint 2 Review y backlog Sprint 3 (PM-03)
5. **Joseph** — revisar y aprobar PRs conforme el equipo los abra en Sprint 3

---

*Última actualización: 5 de julio de 2026 — Joseph*
*Actualizar al cerrar cada sprint o cuando cambien roles, stack o decisiones importantes.*

## 12. Estado al 15 de julio de 2026 (última actualización)

### Despliegue
- Frontend: https://dev-brain-front-end.vercel.app ✅
- Backend: https://devbrain-backend-nrpg.onrender.com ✅ (Live)
- Base de datos: Supabase ✅

### Documentos generados (Sprint 4 — Joseph)
- DOC-01 Acta de constitución → DevBrain_DOC01_ActaConstitucion.docx ✅
- DOC-02 Plan de administración → DevBrain_DOC02_PlanAdministracion.docx ✅
- Ambos van en 11-documentacion-final/ del repo DevBrain-ProjectManagement
- Pendiente subirlos por PR: rama docs/reporte-final-secciones-3-4 → develop

### Problema activo — CORS
El frontend en Vercel no puede conectar con el backend en Render.
Error: "No 'Access-Control-Allow-Origin' header is present"
Lo que se hizo:
- Se instaló el paquete cors en el backend
- Se configuró en src/index.ts permitiendo localhost:5173 y dev-brain-front-end.vercel.app
- Se mergeó develop → main en el repo DevBrain-BackEnd
- Render redesplegó exitosamente (commit 0fc6a1f, branch main, "Your service is live")
- PERO el error de CORS persiste en el navegador
Posible causa: el CORS se configuró DESPUÉS de express.json() o el
paquete cors no quedó en el build de producción. Verificar que
src/index.ts tenga app.use(cors({...})) ANTES de app.use(express.json())
y que cors aparezca en dependencies (no devDependencies) del package.json.

### Issues pendientes de Joseph
- FRONT-17 — Gráfica de actividad del equipo en dashboard (bloqueado por CORS)
- DOC-03 — Cierre del proyecto (se redacta al final, cuando todo esté listo)

### Nombres completos del equipo (para documentos)
- Joseph Lucero Vázquez
- Jesús Juárez López
- Vanessa Krystal García Vázquez
- América Carrera Jiménez
- Adolfo Montes Zayas