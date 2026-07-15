# Bitácoras del Proyecto

## Introducción

Las siguientes bitácoras documentan las actividades realizadas durante el desarrollo del proyecto **DevBrain** a lo largo de cuatro sprints. La información presentada se obtuvo a partir de la actividad registrada en GitHub, considerando los commits, Pull Requests e Issues cerrados en los repositorios del Frontend y Backend. Cada sprint incluye las principales actividades realizadas por el equipo, los incidentes ocurridos, las decisiones tomadas y la referencia a los Issues completados.

---

# Sprint 1

**Periodo:** 21 de junio de 2026 – 27 de junio de 2026

## Actividades realizadas

| Fecha | Integrante | Actividad realizada |
|--------|------------|---------------------|
| 21/06/2026 | Joseph-VZ | Creación del repositorio y registro del *Initial Commit* del proyecto. |
| 22/06/2026 | JessAcke | Configuración inicial del Frontend utilizando Vue 3, Vite, Tailwind CSS, Pinia y Vue Router, además de la creación de la estructura base de carpetas. |
| 23/06/2026 | VKrystalDev | Creación de la estructura de carpetas del Backend. |
| 26/06/2026 | VKrystalDev | Inicialización del Backend con Express y TypeScript. |
| 27/06/2026 | VKrystalDev | Diseño e implementación del esquema inicial de PostgreSQL. |
| 27/06/2026 | VKrystalDev | Creación del archivo `.env.example` para facilitar la configuración del entorno. |

### Incidentes relevantes

- Se estableció la estructura inicial del proyecto para permitir el trabajo colaborativo mediante ramas.
- Se definió el flujo de integración utilizando Pull Requests antes de fusionar cambios al repositorio principal.

### Decisiones tomadas

- Utilizar Express y TypeScript para el Backend.
- Utilizar Vue 3, Vite, Pinia y Tailwind CSS para el Frontend.
- Emplear PostgreSQL como gestor de base de datos.
- Administrar la configuración mediante archivos `.env`.

### Issues completados

#### Backend

- Issue #1 – Crear estructura de carpetas en DevBrain-Backend.
- Issue #2 – Configurar Node.js + Express + TypeScript.
- Issue #3 – Diseñar e implementar el esquema inicial de PostgreSQL.
- Issue #4 – Crear archivo `.env.example`.

#### Frontend

- Issue #1 – Crear estructura de carpetas en DevBrain-Frontend.
- Issue #2 – Configurar Vite + Vue 3 + Tailwind CSS.
- Issue #3 – Configurar Pinia y Vue Router.

---

# Sprint 2

**Periodo:** 28 de junio de 2026 – 5 de julio de 2026

## Actividades realizadas

| Fecha | Integrante | Actividad realizada |
|--------|------------|---------------------|
| 30/06/2026 | VKrystalDev | Configuración de la conexión con Supabase. |
| 30/06/2026 | VKrystalDev | Documentación de variables de entorno y guía de despliegue. |
| 01/07/2026 | ame-97 | Desarrollo de los endpoints de autenticación. |
| 01/07/2026 | ame-97 | Implementación del middleware de autenticación JWT. |
| 03/07/2026 | ame-97 | Desarrollo del CRUD de proyectos protegido mediante JWT. |
| 03/07/2026 | JessAcke | Corrección del proceso de autenticación JWT. |
| 03/07/2026 | JessAcke | Desarrollo del Dashboard y del módulo de Login del Frontend. |
| 04/07/2026 | JessAckerman | Integración del módulo de Login mediante Pull Request. |
| 05/07/2026 | VKrystalDev | Implementación de los endpoints para decisiones. |
| 05/07/2026 | VKrystalDev | Implementación del endpoint de votación. |
| 05/07/2026 | ame-97 | Integración de Gemini AI con contexto de decisiones. |

### Incidentes relevantes

- Se integraron múltiples Pull Requests para consolidar las funcionalidades desarrolladas durante el sprint.
- Se realizaron ajustes al sistema de autenticación antes de continuar con nuevas funcionalidades.

### Decisiones tomadas

- Proteger todos los servicios mediante JWT.
- Integrar Supabase como servicio para la base de datos.
- Incorporar Gemini AI para apoyar el análisis de decisiones del proyecto.
- Mantener un flujo de trabajo basado en ramas y Pull Requests.

### Issues completados

#### Backend

- Issue #9 – Desplegar base de datos en Supabase.
- Issue #10 – Implementar endpoints de autenticación.
- Issue #11 – Implementar middleware JWT.
- Issue #12 – Implementar CRUD de proyectos.
- Issue #13 – Documentar variables de entorno.
- Issue #14 – Documentar endpoints implementados.

#### Frontend

- Issue #5 – Implementar vista de Login.
- Issue #6 – Implementar vista de lista de proyectos.
- Issue #7 – Implementar formulario de creación de proyectos.
- Issue #8 – Configurar rutas protegidas.
- Issue #9 – Implementar interceptor JWT.
- Issue #10 – Pruebas de Login y proyectos.

---

# Sprint 3

**Periodo:** 6 de julio de 2026 – 12 de julio de 2026

## Actividades realizadas

| Fecha | Integrante | Actividad realizada |
|--------|------------|---------------------|
| 05/07/2026 | VKrystalDev | Implementación de los endpoints de decisiones y votaciones. |
| 05/07/2026 | ame-97 | Integración de Gemini AI mediante el endpoint `/ai/query`. |
| 09/07/2026 | JessAcke | Desarrollo de los endpoints de votos e invitaciones en el Backend. |
| 09/07/2026 | JessAcke | Implementación del módulo de decisiones, votaciones e invitaciones en el Frontend. |
| 09/07/2026 | ZAYASNVP | Integración de la vista DevBrain AI en el Frontend. |
| 09/07/2026 | Equipo | Integración de los Pull Requests correspondientes a las funcionalidades desarrolladas durante el sprint. |
| 12/07/2026 | ame-97 | Eliminación de archivos duplicados del Backend. |
| 12/07/2026 | ame-97 | Reversión del Pull Request para recuperar los archivos eliminados accidentalmente. |
| 12/07/2026 | JessAcke | Integración de mejoras relacionadas con estados, comentarios, búsqueda, votaciones e IA con memoria en el Frontend. |

### Incidentes relevantes

- Se detectó la eliminación de archivos duplicados en el Backend, lo que ocasionó la necesidad de revertir un Pull Request para restaurar el proyecto.
- Se fusionaron diversos Pull Requests hacia las ramas principales para consolidar las funcionalidades implementadas.

### Decisiones tomadas

- Reforzar la revisión del código antes de fusionar cambios.
- Mantener sincronizado el desarrollo entre Frontend y Backend.
- Documentar los nuevos endpoints implementados.

### Issues completados

#### Backend

- Issue #23 – Implementar endpoints CRUD de decisiones.
- Issue #24 – Implementar endpoint de votación.
- Issue #25 – Integrar Gemini API.
- Issue #26 – Documentar endpoints de decisiones, votación e IA.

#### Frontend

- Issue #13 – Implementar vista de registro de decisiones.
- Issue #14 – Implementar vista de votación.
- Issue #15 – Implementar vista de timeline.
- Issue #16 – Implementar vista de consulta IA.
- Issue #17 – Pruebas de decisiones y votación.
- Issue #18 – Pruebas de integración Frontend–Backend.

---

# Sprint 4

**Periodo:** 13 de julio de 2026 – 14 de julio de 2026

## Actividades realizadas

| Fecha | Integrante | Actividad realizada |
|--------|------------|---------------------|
| 12/07/2026 | JessAcke | Integración de mejoras de IA, comentarios, búsqueda y votaciones en el Frontend. |
| 13/07/2026 | JessAcke | Integración del sistema de estados, comentarios, búsqueda, votaciones e IA con memoria en el Backend. |
| 13/07/2026 | Joseph-VZ | Despliegue del Backend en Render y coordinación de la migración de invitaciones en Supabase. |
| 14/07/2026 | VKrystalDev | Desarrollo del endpoint de estadísticas del proyecto. |
| 14/07/2026 | VKrystal | Integración del módulo de estadísticas mediante el Pull Request #39. |
| 14/07/2026 | Equipo | Validación final del sistema antes de la entrega del proyecto. |

### Incidentes relevantes

- Se resolvió un problema de conectividad IPv6 entre Render y Supabase durante el despliegue.
- Se realizaron pruebas finales para validar la integración entre Frontend y Backend.

### Decisiones tomadas

- Desplegar el Backend en Render y el Frontend en Vercel para facilitar el acceso al sistema.
- Incorporar un módulo de estadísticas para ofrecer métricas del proyecto.
- Consolidar todos los cambios en la rama `develop` antes de la entrega final.

### Issues completados

#### Backend

- Issue #31 – Desplegar Backend en Render.
- Issue #32 – Ejecutar migración de invitaciones en Supabase.
- Issue #33 – Eliminar archivos duplicados del Backend.
- Issue #34 – Resolver la conexión IPv6 entre Render y Supabase.
- Issue #37 – Implementar estados, votos, comentarios, búsqueda e IA con memoria.
- Issue #38 – Implementar endpoints de estadísticas del proyecto.

#### Frontend

- Issue #22 – Desplegar Frontend en Vercel.
- Issue #24 – Implementar decisiones, votación e invitaciones.
- Issue #25 – Implementar estado, votos, comentarios, búsqueda e IA con memoria.