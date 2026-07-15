# API Contract — DevBrain

Contrato de la API REST que consume el frontend (Vue 3) desde el backend (Node.js/Express).

## 1. Tabla resumen

| Método | Ruta | Auth | Descripción |
|---|---|---|---|
| POST | `/auth/register` | No | Registra un nuevo usuario |
| POST | `/auth/login` | No | Inicia sesión y devuelve un JWT |
| GET | `/projects` | Sí | Lista los proyectos del usuario autenticado |
| POST | `/projects` | Sí | Crea un nuevo proyecto |
| GET | `/projects/:id/stats` | Sí | Estadísticas del proyecto para el dashboard |
| GET | `/decisions?projectId=` | Sí | Lista las decisiones de un proyecto |
| POST | `/decisions` | Sí | Registra una nueva decisión |
| PATCH | `/decisions/:id/status` | Sí | Actualiza el estado de una decisión |
| GET | `/decisions/search?projectId=&q=` | Sí | Busca decisiones por texto |
| GET | `/decisions/:id/comments` | Sí | Lista comentarios de una decisión |
| POST | `/decisions/:id/comments` | Sí | Agrega un comentario a una decisión |
| POST | `/votes` | Sí | Registra el voto de un usuario sobre una decisión |
| POST | `/ai/query` | Sí | Consulta en lenguaje natural sobre decisiones del proyecto |
| POST | `/invitations` | Sí | Invita a un usuario a un proyecto por email |
| GET | `/invitations/:token/accept` | No | Acepta una invitación por token |

---

## 2. Detalle de cada endpoint

### POST `/auth/register`

**Body:**
```json
{ "email": "joseph@example.com", "password": "contraseña123", "name": "Joseph" }
```
**Respuesta exitosa (201):**
```json
{ "id": "uuid-del-usuario", "email": "joseph@example.com", "name": "Joseph" }
```
**Error (400):** `{ "error": "El correo ya está registrado" }`

---

### POST `/auth/login`

**Body:**
```json
{ "email": "joseph@example.com", "password": "contraseña123" }
```
**Respuesta exitosa (200):**
```json
{ "token": "jwt-token-aqui", "user": { "id": "uuid", "email": "joseph@example.com", "name": "Joseph" } }
```
**Error (401):** `{ "error": "Credenciales inválidas" }`

---

### GET `/projects`
**Headers:** `Authorization: Bearer <token>`

**Respuesta exitosa (200):**
```json
[{ "id": "uuid-proyecto-1", "name": "DevBrain", "description": "...", "createdAt": "2026-06-18T10:00:00Z" }]
```

---

### POST `/projects`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{ "name": "DevBrain", "description": "Plataforma de gestión de decisiones técnicas" }
```
**Respuesta exitosa (201):**
```json
{ "id": "uuid-proyecto-1", "name": "DevBrain", "description": "...", "createdAt": "2026-06-18T10:00:00Z" }
```

---

### GET `/projects/:id/stats`
**Headers:** `Authorization: Bearer <token>`

**Respuesta exitosa (200):**
```json
{
  "totalDecisiones": 10,
  "aprobadas": 5,
  "rechazadas": 2,
  "pendientes": 3,
  "totalVotos": 24,
  "totalMiembros": 4,
  "porMiembro": [
    { "userId": 14, "name": "Joseph", "decisionesPropuestas": 3, "votosEmitidos": 5 },
    { "userId": 15, "name": "Vanessa", "decisionesPropuestas": 2, "votosEmitidos": 7 }
  ]
}
```
**Error (404):** `{ "error": "Proyecto no encontrado" }`

---

### GET `/decisions?projectId=`
**Headers:** `Authorization: Bearer <token>`

**Respuesta exitosa (200):**
```json
[{
  "id": "uuid-decision-1",
  "title": "Migrar de MySQL a PostgreSQL",
  "description": "Se necesita soporte para tipos de datos JSON avanzados",
  "alternatives": ["Mantener MySQL", "Migrar a PostgreSQL", "Migrar a MongoDB"],
  "status": "aprobada",
  "proposedBy": "uuid-del-usuario",
  "createdAt": "2026-06-20T14:30:00Z"
}]
```

---

### POST `/decisions`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{
  "projectId": "uuid-proyecto-1",
  "title": "Migrar de MySQL a PostgreSQL",
  "description": "Se necesita soporte para tipos de datos JSON avanzados",
  "alternatives": ["Mantener MySQL", "Migrar a PostgreSQL", "Migrar a MongoDB"]
}
```
**Respuesta exitosa (201):**
```json
{ "id": "uuid-decision-1", "projectId": "uuid-proyecto-1", "title": "...", "createdAt": "2026-06-20T14:30:00Z" }
```

---

### PATCH `/decisions/:id/status`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{ "status": "aprobada" }
```
`status` acepta: `"pendiente"`, `"aprobada"`, `"rechazada"`

**Respuesta exitosa (200):**
```json
{ "id": "uuid-decision-1", "status": "aprobada" }
```

---

### GET `/decisions/search?projectId=&q=`
**Headers:** `Authorization: Bearer <token>`

**Query params:** `projectId` (requerido), `q` (texto a buscar)

**Respuesta exitosa (200):**
```json
[{ "id": "uuid-decision-1", "title": "Migrar de MySQL a PostgreSQL", "description": "..." }]
```

---

### GET `/decisions/:id/comments`
**Headers:** `Authorization: Bearer <token>`

**Respuesta exitosa (200):**
```json
[{ "id": "uuid-comment-1", "text": "Buen argumento", "userId": "uuid", "name": "Joseph", "createdAt": "2026-07-01T10:00:00Z" }]
```

---

### POST `/decisions/:id/comments`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{ "text": "Buen argumento a favor de la migración" }
```
**Respuesta exitosa (201):**
```json
{ "id": "uuid-comment-1", "text": "Buen argumento a favor de la migración", "createdAt": "2026-07-01T10:00:00Z" }
```

---

### POST `/votes`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{ "decisionId": "uuid-decision-1", "vote": "approve" }
```
`vote` acepta: `"approve"` o `"reject"`

**Respuesta exitosa (201):**
```json
{ "decisionId": "uuid-decision-1", "userId": "uuid-del-usuario", "vote": "approve" }
```
**Error (409):** `{ "error": "El usuario ya votó en esta decisión" }`

---

### POST `/ai/query`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{ "projectId": "uuid-proyecto-1", "question": "¿Por qué se migró de MySQL a PostgreSQL?" }
```
**Respuesta exitosa (200):**
```json
{ "answer": "Se migró de MySQL a PostgreSQL porque el equipo necesitaba soporte avanzado para tipos de datos JSON..." }
```
**Error (500):** `{ "error": "No se pudo procesar la consulta de IA en este momento" }`

---

### POST `/invitations`
**Headers:** `Authorization: Bearer <token>`

**Body:**
```json
{ "projectId": "uuid-proyecto-1", "email": "vanessa@devbrain.com", "role": "miembro" }
```
**Respuesta exitosa (201):**
```json
{ "message": "Invitación enviada a vanessa@devbrain.com" }
```
**Error (400):** `{ "error": "El usuario ya es miembro del proyecto" }`

---

### GET `/invitations/:token/accept`
No requiere autenticación — el token en la URL valida la invitación.

**Respuesta exitosa (200):**
```json
{ "message": "Invitación aceptada. Ya eres miembro del proyecto." }
```
**Error (400):** `{ "error": "Token de invitación inválido o expirado" }`

---

## 3. Notas generales

- Todas las rutas protegidas requieren el header `Authorization: Bearer <token>`.
- Los errores siempre se devuelven con la forma `{ "error": "mensaje" }`.
- Las fechas se devuelven en formato ISO 8601 (`YYYY-MM-DDTHH:mm:ssZ`).
- Este contrato refleja el estado final del MVP incluyendo los endpoints implementados en Sprint 3 y Sprint 4.

*Última actualización: 15 de julio de 2026*
