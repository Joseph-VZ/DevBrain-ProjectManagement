# Sprint Backlog — Sprint 3: Features principales

**Periodo:** 2 – 8 de julio de 2026
**Objetivo:** Implementar las funcionalidades core de DevBrain: registro de decisiones, sistema de votación, timeline cronológico e integración con Gemini API, dejando el sistema funcional de punta a punta.

---

## 1. Issues arrastrados de Sprint 2

Ninguno — Sprint 2 se cerró con todos sus issues completados.

## 2. Issues de Sprint 3

| Código | # GitHub | Título | Asignado | Repo | Estado inicial |
|---|---|---|---|---|---|
| BACK-07 | — | Endpoints CRUD de decisiones | Vanessa | Backend | ⏳ Pendiente |
| BACK-08 | — | Endpoint de votación | Vanessa | Backend | ⏳ Pendiente |
| BACK-09 | — | Integrar Gemini API (/ai/query) | América | Backend | ⏳ Pendiente |
| BACK-10 | — | Documentar endpoints decisiones/votación/IA | América + Joseph | ProjectManagement | ⏳ Pendiente |
| FRONT-07 | — | Vista de registro de decisiones | Jesús | Frontend | ⏳ Pendiente |
| FRONT-08 | — | Vista de votación | Jesús | Frontend | ⏳ Pendiente |
| FRONT-09 | — | Vista de timeline cronológico | Jesús | Frontend | ⏳ Pendiente |
| FRONT-10 | — | Vista de consulta IA | Adolfo | Frontend | ⏳ Pendiente |
| FRONT-11 | — | Pruebas de decisiones, votación y timeline | Adolfo | Frontend | ⏳ Pendiente |
| FRONT-12 | — | Pruebas de integración frontend-backend | Adolfo | Frontend | ⏳ Pendiente |
| PM-03 | — | Minuta Sprint 2 Review + backlog Sprint 3 | Joseph | ProjectManagement | ⏳ Pendiente |

> Nota: Actualizar los números de issue de GitHub (#) una vez que estén creados en el repositorio correspondiente.

## 3. Distribución de carga por integrante

| Integrante | Issues | Área |
|---|---|---|
| Joseph | PM-03 | Gestión |
| Jesús | FRONT-07, FRONT-08, FRONT-09 | Frontend |
| Vanessa | BACK-07, BACK-08 | Backend — decisiones y votación |
| América | BACK-09, BACK-10 | Backend — IA y documentación |
| Adolfo | FRONT-10, FRONT-11, FRONT-12 | Frontend + QA |

## 4. Dependencias clave

- **BACK-07 y BACK-08 bloquean a Jesús:** Los endpoints de decisiones y votación deben estar listos antes de que Jesús conecte FRONT-07, FRONT-08 y FRONT-09.
- **BACK-09 bloquea a Adolfo:** El endpoint de IA debe estar funcional antes de que Adolfo empiece FRONT-10 y FRONT-12.
- **FRONT-11 depende de FRONT-07, FRONT-08 y FRONT-09:** Adolfo prueba los flujos cuando Jesús los tenga listos.
- **BACK-10 depende de BACK-09:** América actualiza el API_CONTRACT.md una vez que su implementación de IA esté terminada.

## 5. Tareas previas al inicio del sprint

- [ ] América y Vanessa limpian archivos duplicados en Backend antes de empezar sus issues
- [ ] América configura GEMINI_API_KEY en .env antes de empezar BACK-09
- [ ] Joseph actualiza números de issue reales en esta tabla una vez creados en GitHub

## 6. Notas

- Este sprint es el más crítico del proyecto — contiene las funcionalidades diferenciadoras de DevBrain (decisiones, votación, IA).
- Si el tiempo comienza a escasear, el orden de prioridad para recortar es: timeline visual (puede ser lista simple), sistema de votación (puede simplificarse a campo de estado), nunca recortar la integración con IA (es el diferenciador principal).
