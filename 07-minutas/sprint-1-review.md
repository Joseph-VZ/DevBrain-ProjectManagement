# Minuta — Sprint 1 Review

**Fecha:** 24 de junio de 2026
**Sprint:** Sprint 1 — Planeación y Setup
**Modalidad:** Reunión de cierre
**Asistentes:** Joseph, Jesús, Vanessa, América, Adolfo

---

## 1. Issues completados en Sprint 1

| # | Título | Asignado | Repo |
|---|---|---|---|
| #1 | Investigación del problema y objetivos | Joseph | ProjectManagement |
| #2 | Redactar requerimientos funcionales y no funcionales | Vanessa / América | ProjectManagement |
| #3 | Análisis de actores y casos de uso (UML) | Zayas | ProjectManagement |
| #4 | Revisión e integración del análisis | Jesús | ProjectManagement |
| #5 | Crear estructura de carpetas en ProjectManagement | Joseph | ProjectManagement |
| #6 | Configurar GitHub Project | Joseph | ProjectManagement |
| #7 | Crear diagrama de arquitectura general | Joseph | ProjectManagement |
| #9 | Redactar API_CONTRACT.md | Joseph / Vanessa | ProjectManagement |
| #10 | Elaborar Gantt del proyecto | América | ProjectManagement |
| #11 | Elaborar matriz de riesgos | Adolfo | ProjectManagement |
| #12 | Redactar acta de kickoff | Joseph | ProjectManagement |
| #13 | Crear estructura de carpetas en Frontend | Jesús | Frontend |
| #14 | Configurar Vite + Vue 3 + Tailwind CSS | Jesús | Frontend |
| #15 | Configurar Pinia y Vue Router base | Jesús | Frontend |
| #16 | Crear estructura de carpetas en Backend | Vanessa | Backend |
| #17 | Configurar Node.js + Express + TypeScript | Vanessa | Backend |
| #18 | Diseñar schema inicial de PostgreSQL | Vanessa | Backend |
| #19 | Crear variables de entorno (.env.example) | Vanessa | Backend |

**Total completados:** 18 de 19 issues planeados.

## 2. Issues pendientes arrastrados a Sprint 2

| # | Título | Motivo | Resolución |
|---|---|---|---|
| #8 | Crear diagrama entidad-relación | Vanessa estaba cargada con tareas técnicas de backend | Se arrastra a inicio de Sprint 2 |

## 3. Observaciones del sprint

- El equipo completó el 95% del Sprint 1 en tiempo.
- Se detectó que América y Adolfo tuvieron menor carga de trabajo que el resto. Para Sprint 2 se redistribuyó el trabajo: América implementa toda la API del backend (auth, middleware JWT y CRUD de proyectos), mientras Vanessa se enfoca en base de datos y su documentación. Adolfo participa en código frontend además de pruebas.
- Se corrigió un typo en el nombre del repo: `DevBrain-ProjectManagment` → `DevBrain-ProjectManagement`.
- El flujo de ramas y Pull Requests funcionó correctamente en general. Se reforzó la regla de verificar que el PR apunte a `develop` y no a `main`.

## 4. Distribución de trabajo en Sprint 2

| Integrante | Área | Issues asignados |
|---|---|---|
| Vanessa | Base de datos | BACK-01, BACK-05 |
| América | API backend | BACK-02, BACK-03, BACK-04, BACK-06 |
| Jesús | Frontend | FRONT-01, FRONT-02, FRONT-03 |
| Adolfo | Frontend + QA | FRONT-04, FRONT-05, FRONT-06 |
| Joseph | Gestión | PM-01, PM-02 |

## 5. Acuerdos para Sprint 2

1. Vanessa inicia desplegando la BD en Supabase antes de avanzar en cualquier otra tarea.
2. América revisa el API_CONTRACT.md antes de implementar — si detecta algo inconsistente, lo comunica al equipo antes de codificar.
3. Adolfo participa en código frontend (rutas protegidas + interceptor JWT) además de las pruebas.
4. Todo PR requiere al menos una aprobación antes de merge — sin excepciones a partir de este sprint.
5. Joseph redacta minuta y backlog de Sprint 2 al inicio del sprint.

---

**Próxima reunión:** Sprint 2 Review — 1 de julio de 2026
