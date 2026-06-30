# Diagrama de Arquitectura General — DevBrain

![Arquitectura general de DevBrain](./diagrama-arquitectura.png)

## 1. Capas del sistema

### Cliente
- **Tecnología:** Vue 3, Pinia (estado global), Vue Router (navegación)
- **Despliegue:** Vercel
- Consume la API REST mediante peticiones HTTPS y muestra la interfaz al usuario.

### API REST
- **Tecnología:** Node.js, Express, TypeScript
- **Despliegue:** Render
- Compuesta por tres capas internas:
  - **Middleware:** valida la autenticación mediante JWT en cada petición protegida.
  - **Controladores:** manejan la lógica de cada recurso (`auth`, `projects`, `decisions`, `votes`, `ai`).
  - **Servicios:** lógica de negocio reutilizable, incluyendo `authService` y `aiService`.

### Base de datos
- **Tecnología:** PostgreSQL, alojada en Supabase
- Almacena usuarios, proyectos, decisiones y votos mediante modelos con queries SQL directas (sin ORM).

### Integración con IA
- **Tecnología:** Gemini API
- El cliente Gemini, dentro del backend, construye el prompt de contexto y lo envía a la API.
- **Importante:** Gemini nunca accede directamente a la base de datos. Toda la información que recibe ya fue consultada y preparada por el backend.

## 2. Flujo de una consulta a la IA

1. El usuario escribe una pregunta en lenguaje natural desde el frontend.
2. El frontend envía la pregunta al endpoint `/ai/query` de la API REST.
3. El backend consulta en PostgreSQL las decisiones del proyecto activo.
4. El backend construye un prompt que incluye esa información como contexto.
5. El prompt se envía a la API de Gemini.
6. Gemini genera una respuesta en lenguaje natural, que el backend devuelve al frontend.
7. El frontend muestra la respuesta al usuario.

## 3. Justificación de las decisiones de arquitectura

- **Separación cliente/servidor:** permite desplegar frontend y backend de forma independiente (Vercel y Render respectivamente), cada uno escalando según sus propias necesidades.
- **JWT para autenticación:** evita mantener sesiones en el servidor, lo cual simplifica el despliegue en un entorno serverless/gratuito como Render.
- **PostgreSQL como única fuente de verdad:** todas las decisiones, votos y proyectos se almacenan de forma relacional, lo que garantiza consistencia de datos antes de enviarlos como contexto a la IA.
- **Gemini sin acceso directo a la base de datos:** por seguridad y control — el backend decide exactamente qué información se expone a la IA en cada consulta.
