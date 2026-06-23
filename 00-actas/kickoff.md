# Acta de Kickoff — Proyecto DevBrain

**Materia:** Administración de Proyectos para TI
**Fecha de la reunión:** 18 de junio de 2026
**Modalidad:** Videoconferencia
**Duración:** ~60 minutos

## Asistentes

| Nombre | Rol |
|---|---|
| Joseph | Líder del proyecto, gestión e integración final |
| Jesús | Responsable Frontend, diseño UI/UX |
| Vanessa | Responsable Backend |
| América | Responsable de análisis y documentación |
| Adolfo | Responsable QA y pruebas |

Los 5 integrantes del equipo estuvieron presentes.

## Objetivo de la reunión

Arrancar formalmente el proyecto DevBrain: alinear al equipo sobre el alcance, definir roles, establecer el stack tecnológico y acordar la forma de trabajo en GitHub para las próximas 4 semanas.

## Temas tratados

### 1. Repartición de roles y responsabilidades

Se asignó un rol principal a cada integrante, con el acuerdo de que **nadie trabaja de forma aislada** — todos participan en desarrollo, documentación, revisión y pruebas en alguna medida durante el proyecto:

- **Joseph** — Liderazgo general, gestión del repositorio de documentación, integración final
- **Jesús** — Frontend (Vue 3), diseño de interfaz
- **Vanessa** — Backend (Node.js/Express), base de datos
- **América** — Análisis de requerimientos, documentación
- **Adolfo** — Aseguramiento de calidad y pruebas

### 2. Stack tecnológico y arquitectura

Se acordó el stack tecnológico del proyecto:

- **Frontend:** Vue 3, Pinia, Vue Router, Tailwind CSS
- **Backend:** Node.js, Express, TypeScript
- **Base de datos:** PostgreSQL (Supabase)
- **Autenticación:** JWT
- **IA:** Gemini API, para consultas en lenguaje natural sobre el historial de decisiones
- **Despliegue:** Vercel (frontend) y Render (backend)

Se decidió dividir el proyecto en 3 repositorios independientes —`DevBrain-Frontend`, `DevBrain-Backend` y `DevBrain-ProjectManagement`— para mantener una estructura ordenada y profesional.

### 3. Metodología y flujo de trabajo en GitHub

Se explicó al equipo la metodología de trabajo:

- **Metodología:** Scrum ligero combinado con Kanban, usando GitHub Projects
- **Flujo de ramas:** `main` (estable) y `develop` (integración diaria); todo el trabajo se hace en ramas `feature/`, `fix/` o `docs/`
- **Regla principal:** ningún integrante hace push directo a `main` ni a `develop` — todo cambio entra mediante Pull Request con al menos una aprobación
- **Seguimiento:** tablero Kanban centralizado en `DevBrain-ProjectManagement`, con columnas Backlog, Sprint Actual, En Progreso, En Revisión, Completado y Bloqueado

## Acuerdos alcanzados

1. El proyecto se organiza en 4 sprints semanales, del 18 de junio al 12 de julio, con entrega final el 14 de julio
2. Cada integrante revisará el documento de flujo de trabajo (`Guia-Flujo-Trabajo-DevBrain.md`) antes de su primer commit
3. Las reuniones de seguimiento serán: daily asíncrono por mensaje, sync técnico martes/jueves, y Sprint Review los domingos de cierre de sprint
4. Joseph queda como responsable de aprobar los Pull Requests hacia `main`

## Próximos pasos

- Completar configuración de los 3 repositorios (ramas protegidas, labels, milestones)
- Crear y asignar los issues del Sprint 1
- Iniciar redacción de requerimientos funcionales y no funcionales
