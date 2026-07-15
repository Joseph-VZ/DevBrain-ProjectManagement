# Reporte de lenguajes y tecnologías utilizadas

## Introducción

El desarrollo de **DevBrain** se apoyó en un conjunto de tecnologías modernas orientadas al desarrollo de aplicaciones web bajo una arquitectura cliente-servidor. La selección de cada herramienta se realizó considerando criterios como facilidad de integración, estabilidad, escalabilidad, documentación disponible, soporte de la comunidad y disponibilidad de planes gratuitos para proyectos académicos.

La combinación de estas tecnologías permitió construir una plataforma colaborativa para la gestión del conocimiento técnico, integrando un frontend moderno, una API REST segura, una base de datos relacional administrada en la nube y servicios de despliegue continuo.

---

## Frontend

### Vue
- **Versión:** 3.5.13
- **Capa:** Frontend
- **Justificación:** Framework progresivo basado en componentes que facilita el desarrollo de interfaces reactivas, reutilizables y de fácil mantenimiento. Constituye la base de toda la interfaz de usuario del sistema.

### Pinia
- **Versión:** 2.2.6
- **Capa:** Frontend
- **Justificación:** Biblioteca oficial para la administración del estado global en aplicaciones Vue. Permite compartir información entre componentes de forma sencilla y organizada.

### Vue Router
- **Versión:** 4.4.5
- **Capa:** Frontend
- **Justificación:** Gestiona la navegación entre las diferentes vistas del sistema y controla el acceso a rutas protegidas mediante autenticación.

### Tailwind CSS
- **Versión:** 4.0.0
- **Capa:** Frontend
- **Justificación:** Framework CSS utilitario que permitió desarrollar una interfaz moderna, responsiva y consistente, reduciendo la necesidad de escribir hojas de estilo extensas.

### Axios
- **Versión:** 1.18.1
- **Capa:** Frontend
- **Justificación:** Cliente HTTP utilizado para establecer la comunicación entre el frontend y la API REST del backend mediante solicitudes autenticadas.

---

## Backend

### Node.js
- **Versión:** 22.x LTS
- **Capa:** Backend
- **Justificación:** Entorno de ejecución que permite desarrollar aplicaciones del lado del servidor utilizando JavaScript y TypeScript, ofreciendo un buen rendimiento para APIs REST.

### Express
- **Versión:** 5.2.1
- **Capa:** Backend
- **Justificación:** Framework minimalista utilizado para construir la API REST del sistema con una arquitectura modular y fácil de mantener.

### TypeScript
- **Versión:** 6.0.3
- **Capa:** Backend
- **Justificación:** Lenguaje basado en JavaScript que incorpora tipado estático, mejorando la calidad del código y reduciendo errores durante el desarrollo.

### dotenv
- **Versión:** 17.4.2
- **Capa:** Backend
- **Justificación:** Permite administrar las variables de entorno utilizadas por la aplicación, evitando almacenar información sensible dentro del código fuente.

### JSON Web Token (JWT)
- **Versión:** 9.0.3
- **Capa:** Backend
- **Justificación:** Implementa el mecanismo de autenticación y autorización mediante tokens, protegiendo los recursos del sistema.

### bcryptjs
- **Versión:** 3.0.3
- **Capa:** Backend
- **Justificación:** Biblioteca utilizada para cifrar las contraseñas mediante funciones hash antes de almacenarlas en la base de datos.

### pg
- **Versión:** 8.22.0
- **Capa:** Backend
- **Justificación:** Cliente oficial de PostgreSQL para Node.js, encargado de administrar las conexiones y consultas hacia la base de datos.

### Nodemailer
- **Versión:** 9.0.3
- **Capa:** Backend
- **Justificación:** Biblioteca utilizada para el envío de correos electrónicos, principalmente para la gestión de invitaciones a proyectos.

---

## Base de datos

### PostgreSQL
- **Versión:** 16
- **Capa:** Base de datos
- **Justificación:** Sistema gestor de bases de datos relacional utilizado para almacenar de forma segura toda la información del sistema.

### Supabase
- **Versión:** Plataforma
- **Capa:** Base de datos
- **Justificación:** Servicio administrado que proporciona el alojamiento de PostgreSQL y herramientas para facilitar la administración de la base de datos en la nube.

---

## Inteligencia Artificial

### @google/generative-ai (Gemini API)
- **Versión:** 0.24.1
- **Capa:** Inteligencia Artificial
- **Justificación:** SDK oficial utilizado para integrar Gemini API dentro de DevBrain, permitiendo responder consultas inteligentes basadas en las decisiones técnicas registradas en el sistema.

---

## Despliegue y gestión del proyecto

### Vercel
- **Versión:** Plataforma
- **Capa:** Despliegue
- **Justificación:** Plataforma utilizada para publicar automáticamente el frontend mediante integración continua con GitHub.

### Render
- **Versión:** Plataforma
- **Capa:** Despliegue
- **Justificación:** Servicio utilizado para desplegar y mantener disponible la API REST del backend.

### GitHub
- **Versión:** Plataforma
- **Capa:** Control de versiones
- **Justificación:** Plataforma utilizada para alojar el código fuente, administrar versiones mediante Git y coordinar el trabajo colaborativo mediante Pull Requests.

### GitHub Projects
- **Versión:** Plataforma
- **Capa:** Gestión del proyecto
- **Justificación:** Herramienta empleada para administrar el backlog, organizar tareas y dar seguimiento al avance del desarrollo mediante tableros Kanban.

### Trello
- **Versión:** Plataforma
- **Capa:** Gestión del proyecto
- **Justificación:** Herramienta complementaria utilizada para la planificación y seguimiento de actividades durante el desarrollo del proyecto.

---

## Rol de las tecnologías dentro de la arquitectura

Las tecnologías seleccionadas permitieron implementar una arquitectura cliente-servidor claramente dividida en capas. En el frontend, Vue, Pinia, Vue Router, Tailwind CSS y Axios proporcionan una interfaz interactiva, modular y capaz de comunicarse con la API REST. En el backend, Node.js, Express, TypeScript, dotenv, JWT, bcryptjs, pg y Nodemailer conforman una capa de servicios responsable de la lógica de negocio, autenticación, acceso a datos y comunicación por correo electrónico. PostgreSQL, administrado mediante Supabase, almacena la información persistente del sistema, mientras que @google/generative-ai integra las capacidades de inteligencia artificial para responder consultas sobre el conocimiento registrado. Finalmente, Vercel y Render permiten el despliegue del frontend y backend, mientras que GitHub, GitHub Projects y Trello apoyan el control de versiones y la gestión del proyecto.

---

## Conclusión

La selección de estas tecnologías permitió desarrollar una solución moderna, escalable y mantenible. Cada herramienta cumple un propósito específico dentro de la arquitectura del sistema y, en conjunto, conforman un stack tecnológico que facilita el desarrollo colaborativo, la integración continua y el despliegue de DevBrain.