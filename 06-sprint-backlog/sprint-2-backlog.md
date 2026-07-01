# Sprint Backlog — Sprint 2: Core

**Periodo:** 25 de junio – 1 de julio de 2026
**Objetivo:** Tener el sistema funcional en su base: base de datos desplegada, API de autenticación y proyectos operativa, y el frontend conectado con login y gestión de proyectos.

---

## 1. Issues arrastrados de Sprint 1

| # | Título | Asignado | Estado |
|---|---|---|---|
| #8 | Crear diagrama entidad-relación | Vanessa | 🔄 Integrado en Sprint 2 |

## 2. Issues de Sprint 2

| Código | # GitHub | Título | Asignado | Repo | Estado inicial |
|---|---|---|---|---|---|
| BACK-01 | #20 | Desplegar base de datos en Supabase | Vanessa | Backend | ⏳ Pendiente |
| BACK-02 | #21 | Implementar endpoints de autenticación | América | Backend | ⏳ Pendiente |
| BACK-03 | #22 | Implementar middleware de validación JWT | América | Backend | ⏳ Pendiente |
| BACK-04 | #23 | Implementar endpoints CRUD de proyectos | América | Backend | ⏳ Pendiente |
| BACK-05 | #24 | Documentar variables de entorno y guía de despliegue | Vanessa | Backend | ⏳ Pendiente |
| BACK-06 | #25 | Redactar documentación de endpoints implementados | América | Backend | ⏳ Pendiente |
| FRONT-01 | #26 | Implementar vista de Login | Jesús | Frontend | ⏳ Pendiente |
| FRONT-02 | #27 | Implementar vista de lista de proyectos | Jesús | Frontend | ⏳ Pendiente |
| FRONT-03 | #28 | Implementar formulario de creación de proyecto | Jesús | Frontend | ⏳ Pendiente |
| FRONT-04 | #29 | Configurar rutas protegidas en Vue Router | Adolfo | Frontend | ⏳ Pendiente |
| FRONT-05 | #30 | Implementar interceptor de Axios para JWT | Adolfo | Frontend | ⏳ Pendiente |
| FRONT-06 | #31 | Pruebas de login y proyectos en frontend | Adolfo | Frontend | ⏳ Pendiente |
| PM-01 | #32 | Redactar minuta de Sprint 1 Review | Joseph | ProjectManagement | ⏳ Pendiente |
| PM-02 | #33 | Actualizar backlog con issues reales de Sprint 2 | Joseph | ProjectManagement | ⏳ Pendiente |

**Total de issues:** 14 nuevos + 1 arrastrado = 15 issues en Sprint 2.

## 3. Distribución de carga por integrante

| Integrante | Issues | Área principal |
|---|---|---|
| Joseph | PM-01, PM-02 | Gestión y documentación |
| Jesús | FRONT-01, FRONT-02, FRONT-03 | Frontend |
| Vanessa | BACK-01, BACK-05, #8 | Base de datos |
| América | BACK-02, BACK-03, BACK-04, BACK-06 | API backend |
| Adolfo | FRONT-04, FRONT-05, FRONT-06 | Frontend + QA |

## 4. Dependencias clave

- **BACK-01 bloquea a América:** América no puede probar sus endpoints sin la BD desplegada — Vanessa debe completar BACK-01 primero.
- **BACK-02 y BACK-03 bloquean al frontend:** Jesús y Adolfo no pueden conectar login real hasta que América tenga auth funcionando.
- **FRONT-06 depende de FRONT-01, FRONT-02 y FRONT-03:** Adolfo prueba cuando Jesús termine los flujos principales.

## 5. Notas

- Los números de issue de GitHub (#20 al #33) pueden variar ligeramente según el orden en que se crearon — ajustar si es necesario.
- Al cierre del sprint, actualizar la columna "Estado inicial" con el estado real de cada issue.
EOF