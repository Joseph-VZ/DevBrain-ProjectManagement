# Minuta — Sprint 3 Review

**Fecha:** 9 de julio de 2026
**Sprint:** Sprint 3 — Features principales
**Modalidad:** Reunión de cierre
**Asistentes:** Joseph, Jesús, Vanessa, América, Adolfo

---

## 1. Issues completados en Sprint 3

| Código | Título | Asignado | Repo |
|---|---|---|---|
| BACK-07 | Endpoints CRUD de decisiones | Vanessa | Backend |
| BACK-08 | Endpoint de votación | Vanessa | Backend |
| BACK-09 | Integrar Gemini API (/ai/query) | América | Backend |
| BACK-10 | Documentar endpoints decisiones/votación/IA | América + Joseph | ProjectManagement |
| FRONT-07 | Vista de registro de decisiones | Jesús | Frontend |
| FRONT-08 | Vista de votación | Jesús | Frontend |
| FRONT-09 | Vista de timeline cronológico | Jesús | Frontend |
| FRONT-10 | Vista de consulta IA | Adolfo | Frontend |
| FRONT-11 | Pruebas de decisiones, votación y timeline | Adolfo | Frontend |
| FRONT-12 | Pruebas de integración frontend-backend | Adolfo | Frontend |
| PM-03 | Minuta Sprint 2 Review + backlog Sprint 3 | Joseph | ProjectManagement |

**Total completados:** 11 de 11 issues planeados. ✅

## 2. Issues arrastrados a Sprint 4

Ninguno — todos los issues de Sprint 3 fueron completados.

## 3. Trabajo adicional no planeado

Jesús implementó de forma adicional un sistema completo de invitaciones por email (`invitationController.ts`, `mailer.ts`, `002_invitaciones.sql`), que no estaba en el scope original del sprint pero agrega valor al MVP. Puntos a considerar:

- La migración `002_invitaciones.sql` debe ejecutarse en Supabase antes de que los endpoints de invitación funcionen en producción (tarea BACK-12 en Sprint 4)
- El mailer tiene un modo de desarrollo que imprime los correos en consola si no hay SMTP configurado — no requiere configuración adicional para las pruebas locales

## 4. Observaciones del sprint

- El equipo completó el 100% de los issues planeados por segundo sprint consecutivo — excelente ritmo considerando el tiempo disponible.
- Los nombres de ramas siguen sin seguir la convención acordada (`feature/<numero>-descripcion`). Se refuerza la regla para Sprint 4.
- El flujo de PRs hacia `develop` mejoró notablemente respecto a Sprint 2 — no se detectaron merges directos a `main`.
- La integración con Gemini API quedó funcional con contexto real de decisiones del proyecto.

## 5. Acuerdos para Sprint 4

1. Prioridad absoluta: despliegue en Render (backend) y Vercel (frontend) — sin esto no hay presentación.
2. Vanessa despliega el backend en Render hoy mismo (10 de julio).
3. Jesús ejecuta la migración de invitaciones en Supabase y despliega el frontend en Vercel en cuanto Vanessa comparta la URL de Render.
4. América limpia los archivos duplicados del Backend y redacta el manual de usuario.
5. Adolfo realiza la prueba de humo en producción una vez que ambos despliegues estén listos.
6. El 13 de julio es buffer exclusivo para emergencias — no para desarrollo nuevo.
7. Joseph cierra el sprint con el merge develop → main en los 3 repos el 12 de julio.

---

**Próxima reunión:** Sprint 4 Review / Entrega final — 14 de julio de 2026
