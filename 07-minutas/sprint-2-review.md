# Minuta — Sprint 2 Review

**Fecha:** 4 de julio de 2026
**Sprint:** Sprint 2 — Core
**Modalidad:** Reunión de cierre
**Asistentes:** Joseph, Jesús, Vanessa, América, Adolfo

---

## 1. Issues completados en Sprint 2

| Código | # | Título | Asignado | Repo |
|---|---|---|---|---|
| BACK-01 | #20 | Desplegar base de datos en Supabase | Vanessa | Backend |
| BACK-02 | #21 | Endpoints de autenticación | América | Backend |
| BACK-03 | #22 | Middleware de validación JWT | América | Backend |
| BACK-04 | #23 | Endpoints CRUD de proyectos | América | Backend |
| BACK-05 | #24 | Docs variables de entorno + guía de despliegue | Vanessa | Backend |
| BACK-06 | #25 | Docs endpoints implementados | América | Backend |
| FRONT-01 | #26 | Vista de Login | Jesús | Frontend |
| FRONT-02 | #27 | Vista lista de proyectos | Jesús | Frontend |
| FRONT-03 | #28 | Formulario creación de proyecto | Jesús | Frontend |
| FRONT-04 | #29 | Rutas protegidas Vue Router | Adolfo | Frontend |
| FRONT-05 | #30 | Interceptor Axios JWT | Adolfo | Frontend |
| FRONT-06 | #31 | Pruebas login y proyectos | Adolfo | Frontend |
| PM-01 | #32 | Minuta Sprint 1 Review | Joseph | ProjectManagement |
| PM-02 | #33 | Backlog Sprint 2 | Joseph | ProjectManagement |

**Total completados:** 14 de 14 issues planeados. ✅

## 2. Issues arrastrados a Sprint 3

Ninguno — todos los issues de Sprint 2 fueron completados.

## 3. Observaciones del sprint

### Problemas encontrados
- **PRs mergeados a main en lugar de develop:** Varios PRs de América (BACK-02, BACK-03, BACK-04) y una corrección de Jesús fueron mergeados directamente a `main`. Esto dejó `develop` desactualizado y confundió al equipo al no ver los cambios en la rama correcta. Joseph sincronizó manualmente `develop` con `main` al cierre del sprint.
- **Archivos duplicados en Backend:** Como consecuencia del problema anterior, se crearon archivos duplicados (`projectController.ts` / `projectsController.ts` y `project.routes.ts` / `projects.routes.ts`). Pendiente de limpieza por América y Vanessa al inicio de Sprint 3.
- **Nombres de ramas fuera de convención:** Se usaron nombres como `v1.1-Jess-Login` en lugar del formato acordado `feature/<numero>-descripcion`.
- **Sprint extendido:** Sprint 2 se extendió hasta el 4 de julio (3 días extra) por las correcciones necesarias.

### Lo que funcionó bien
- El equipo completó el 100% de los issues planeados.
- La redistribución de carga (Vanessa = BD, América = API, Adolfo en frontend + QA) funcionó correctamente.
- El sistema de login y gestión de proyectos quedó funcional end-to-end.

## 4. Acuerdos para Sprint 3

1. **Regla reforzada:** Todo PR debe apuntar a `develop`, nunca a `main`. Sin excepciones.
2. **Nombres de ramas:** Usar siempre el formato `feature/<numero-issue>-descripcion-corta`.
3. **América y Vanessa** limpian los archivos duplicados de Backend como primera tarea del sprint.
4. **América** configura `GEMINI_API_KEY` en `.env` antes de empezar el issue de integración con Gemini (BACK-09).
5. **Dependencias a respetar:** Vanessa termina BACK-07 y BACK-08 antes de que Jesús conecte el frontend de decisiones y votación. América termina BACK-09 antes de que Adolfo empiece FRONT-10 y FRONT-12.

---

**Próxima reunión:** Sprint 3 Review — 8 de julio de 2026
