# Sprint Backlog — Sprint 4: Cierre

**Periodo:** 9 – 12 de julio de 2026
**Objetivo:** Desplegar el sistema en producción (Vercel + Render), ejecutar pruebas finales, corregir bugs críticos y completar la documentación requerida para la entrega del 14 de julio.

---

## 1. Issues arrastrados de Sprint 3

Ninguno — Sprint 3 se cerró con todos sus issues completados.

## 2. Issues de Sprint 4

| Código | Título | Asignado | Repo | Prioridad | Estado |
|---|---|---|---|---|---|
| BACK-11 | Desplegar backend en Render | Vanessa | Backend | 🔴 Crítica | ⏳ Pendiente |
| BACK-12 | Ejecutar migración de invitaciones en Supabase | Jesús | Backend | 🔴 Alta | ⏳ Pendiente |
| FRONT-13 | Desplegar frontend en Vercel | Jesús | Frontend | 🔴 Crítica | ⏳ Pendiente |
| FRONT-14 | Prueba de humo del sistema desplegado | Adolfo | Frontend | 🔴 Alta | ⏳ Pendiente |
| FIX-01 | Eliminar archivos duplicados en Backend | América | Backend | 🟡 Media | ⏳ Pendiente |
| PM-05 | Minuta Sprint 3 Review + backlog Sprint 4 | Joseph | ProjectManagement | 🟢 Baja | ⏳ Pendiente |
| PM-06 | Manual de usuario | América | ProjectManagement | 🟡 Media | ⏳ Pendiente |
| PM-07 | Lecciones aprendidas | América | ProjectManagement | 🟢 Baja | ⏳ Pendiente |
| PM-08 | Consolidar documentación final | Joseph | ProjectManagement | 🟡 Media | ⏳ Pendiente |
| PM-09 | Acta de cierre del proyecto | Joseph | ProjectManagement | 🟢 Baja | ⏳ Pendiente |

**Total de issues:** 10

## 3. Distribución de carga por integrante

| Integrante | Issues | Área |
|---|---|---|
| Joseph | PM-05, PM-08, PM-09 | Gestión y documentación final |
| Jesús | BACK-12, FRONT-13 | Migración BD + despliegue Frontend |
| Vanessa | BACK-11 | Despliegue Backend |
| América | FIX-01, PM-06, PM-07 | Corrección + documentación |
| Adolfo | FRONT-14 | QA en producción |

## 4. Dependencias críticas

- **BACK-11 bloquea a todos:** Sin la URL de Render no hay despliegue de frontend ni pruebas en producción.
- **FRONT-13 depende de BACK-11:** Jesús necesita la URL de Render para configurar VITE_API_URL en Vercel.
- **FRONT-14 depende de BACK-11 y FRONT-13:** Adolfo solo puede probar cuando ambos despliegues estén listos.
- **PM-09 depende de BACK-11 y FRONT-13:** El acta de cierre necesita las URLs reales del sistema desplegado.

## 5. Orden de ejecución recomendado

**10 de julio (hoy):**
- Vanessa: BACK-11 (despliegue Render) — prioridad máxima
- Jesús: BACK-12 (migración Supabase) — en paralelo con Vanessa
- América: FIX-01 (archivos duplicados) — puede hacerlo mientras espera URLs
- Joseph: PM-05 (minuta + backlog) — este documento

**11 de julio:**
- Jesús: FRONT-13 (despliegue Vercel) — en cuanto Vanessa comparta la URL de Render
- Adolfo: FRONT-14 (prueba de humo) — en cuanto ambas URLs estén listas
- América: PM-06 (manual de usuario) + PM-07 (lecciones aprendidas)
- Joseph: PM-08 (consolidar documentación)

**12 de julio:**
- Corrección de bugs encontrados por Adolfo en FRONT-14
- Joseph: PM-09 (acta de cierre con URLs reales)
- Joseph: merge develop → main en los 3 repos (cierre oficial Sprint 4)

**13 de julio (buffer):**
- Solo para emergencias — no desarrollo nuevo

## 6. Notas

- Lo que NO se puede recortar bajo ningún concepto: despliegue funcional y manual de usuario.
- Si el despliegue falla el 11 de julio, avisar a Joseph inmediatamente para resolver en conjunto.
- Las URLs finales del sistema (Vercel + Render) deben quedar documentadas en el acta de cierre y en el README principal de ProjectManagement.
