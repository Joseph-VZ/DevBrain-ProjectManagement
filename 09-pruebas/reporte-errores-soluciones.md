# 14. Reporte de errores y soluciones

## 14.1 Introducción

Durante el desarrollo del proyecto **DevBrain** se presentaron diversos problemas técnicos y de gestión que afectaron temporalmente el avance del equipo. Cada uno de estos incidentes fue identificado, analizado y solucionado antes de continuar con el desarrollo.

---

## 14.2 Error 1. Ajustes iniciales de configuración

**Sprint:** Sprint 1

### Descripción:
Durante la configuración inicial del proyecto fue necesario realizar algunos ajustes menores en la estructura de carpetas y en la configuración del entorno de desarrollo para que todos los integrantes trabajaran sobre una misma base. También fue necesario estandarizar la configuración tanto del Frontend como del Backend.

### Causa raíz:
El proyecto comenzó desde cero y fue necesario definir la organización de los repositorios, las herramientas de desarrollo y la estructura general del sistema.

### Solución aplicada:
Se reorganizó la estructura inicial del proyecto, se configuraron correctamente ambos repositorios y se creó el archivo `.env.example` para facilitar la configuración del entorno de desarrollo de todos los integrantes.

---

## 14.3 Error 2. Pull Requests fusionados directamente a la rama main

**Sprint:** Sprint 2

### Descripción:
Durante el segundo sprint algunos Pull Requests fueron fusionados directamente a la rama `main`, cuando el flujo de trabajo establecido indicaba que primero debían integrarse en la rama `develop`.

### Causa raíz:
Al inicio del proyecto no todos los integrantes seguían el mismo flujo de trabajo con Git, lo que ocasionó diferencias en la forma de integrar los cambios.

### Solución aplicada:
Se sincronizaron las ramas `main` y `develop`, se revisó el historial del repositorio y se estableció como regla que todos los cambios debían integrarse primero en `develop` mediante Pull Requests revisados por el equipo.

---

## 14.4 Error 3. Archivos duplicados en el Backend

**Sprint:** Sprint 2

### Descripción:
Durante el desarrollo del Backend se detectó la existencia de archivos duplicados relacionados con el controlador de proyectos (`projectsController.ts` y `projectController.ts`). Esto provocó confusión respecto a cuál archivo debía mantenerse como versión oficial.

### Causa raíz:
La integración de cambios provenientes de distintas ramas generó archivos con nombres similares y funciones duplicadas.

### Solución aplicada:
Se eliminaron los archivos duplicados mediante un Pull Request. Posteriormente fue necesario revertir parte del cambio para recuperar archivos eliminados accidentalmente y finalmente se reorganizó la estructura del Backend dejando únicamente la versión correcta de cada controlador.

---

## 14.5 Error 4. Convención de nombres de ramas

**Sprint:** Sprint 2 – Sprint 3

### Descripción:
Durante los primeros sprints se utilizaron diferentes convenciones para nombrar las ramas del repositorio, por ejemplo `Vista_IA`, `v1.1-Jess-Login` y `feature/...`, lo que dificultaba identificar rápidamente el propósito de cada rama.

### Causa raíz:
No existía una convención de nombres definida desde el inicio del proyecto.

### Solución aplicada:
El equipo acordó utilizar una nomenclatura estándar basada en prefijos como:

- `feature/` para nuevas funcionalidades.
- `fix/` para correcciones de errores.
- `docs/` para cambios en documentación.
- `develop` como rama de integración.

Esto permitió mejorar la organización del repositorio y facilitar el seguimiento de las actividades.

---

## 14.6 Error 5. Problemas de integración entre Frontend, Backend y Gemini AI

**Sprint:** Sprint 3

### Descripción:
Durante la integración del módulo de Inteligencia Artificial y de los nuevos endpoints surgieron problemas de comunicación entre el Frontend y el Backend, debido a diferencias entre las rutas implementadas y las esperadas por la interfaz.

### Causa raíz:
Los servicios del Backend continuaban evolucionando mientras el Frontend se desarrollaba en paralelo, ocasionando inconsistencias temporales en la integración.

### Solución aplicada:
Se actualizaron los endpoints del Backend, se ajustaron las llamadas HTTP realizadas desde el Frontend y se realizaron pruebas de integración para verificar el correcto funcionamiento de todas las funcionalidades.

---

## 14.7 Error 6. Problemas durante el despliegue

**Sprint:** Sprint 4

### Descripción:
Durante el despliegue final del proyecto se presentaron inconvenientes en la conexión entre Render y Supabase, además de ajustes necesarios para completar la publicación del Frontend en Vercel.

### Causa raíz:
La configuración inicial de los servicios en la nube y algunos parámetros de conexión no eran compatibles con la infraestructura utilizada para el despliegue.

### Solución aplicada:
Se corrigió la configuración de conexión entre Render y Supabase, se validó nuevamente el despliegue del Backend y posteriormente se verificó la comunicación con el Frontend desplegado en Vercel mediante pruebas finales de integración.