# API Contract — DevBrain

Contrato de la API REST que consume el frontend (Vue 3) desde el backend (Node.js/Express). Documenta los endpoints mínimos del MVP: método HTTP, ruta, body esperado y respuesta (éxito y error).

## 1. Tabla resumen

| Método | Ruta | Auth requerida | Descripción |
|---|---|---|---|
| POST | `/auth/register` | No | Registra un nuevo usuario |
| POST | `/auth/login` | No | Inicia sesión y devuelve un JWT |
| GET | `/projects` | Sí | Lista los proyectos del usuario autenticado |
| POST | `/projects` | Sí | Crea un nuevo proyecto |
| GET | `/decisions?projectId=` | Sí | Lista las decisiones de un proyecto |
| POST | `/decisions` | Sí | Registra una nueva decisión |
| POST | `/votes` | Sí | Registra el voto de un usuario sobre una decisión |
| POST | `/ai/query` | Sí | Envía una pregunta en lenguaje natural sobre el historial de decisiones |

## 2. Detalle de cada endpoint

### POST `/auth/register`

**Body esperado:**
```json
{
  "email": "joseph@example.com",
  "password": "contraseña123",
  "name": "Joseph"
}
```

**Respuesta exitosa (201):**
```json
{
  "id": "uuid-del-usuario",
  "email": "joseph@example.com",
  "name": "Joseph"
}
```

**Respuesta de error (400):**
```json
{
  "error": "El correo ya está registrado"
}
```

---

### POST `/auth/login`

**Body esperado:**
```json
{
  "email": "joseph@example.com",
  "password": "contraseña123"
}
```

**Respuesta exitosa (200):**
```json
{
  "token": "jwt-token-aqui",
  "user": {
    "id": "uuid-del-usuario",
    "email": "joseph@example.com",
    "name": "Joseph"
  }
}
```

**Respuesta de error (401):**
```json
{
  "error": "Credenciales inválidas"
}
```

---

### GET `/projects`

**Headers requeridos:** `Authorization: Bearer <token>`

**Respuesta exitosa (200):**
```json
[
  {
    "id": "uuid-proyecto-1",
    "name": "DevBrain",
    "description": "Plataforma de gestión de decisiones técnicas",
    "createdAt": "2026-06-18T10:00:00Z"
  }
]
```

**Respuesta de error (401):**
```json
{
  "error": "Token inválido o expirado"
}
```

---

### POST `/projects`

**Headers requeridos:** `Authorization: Bearer <token>`

**Body esperado:**
```json
{
  "name": "DevBrain",
  "description": "Plataforma de gestión de decisiones técnicas"
}
```

**Respuesta exitosa (201):**
```json
{
  "id": "uuid-proyecto-1",
  "name": "DevBrain",
  "description": "Plataforma de gestión de decisiones técnicas",
  "createdAt": "2026-06-18T10:00:00Z"
}
```

**Respuesta de error (400):**
```json
{
  "error": "El nombre del proyecto es obligatorio"
}
```

---

### GET `/decisions?projectId=`

**Headers requeridos:** `Authorization: Bearer <token>`

**Query params:** `projectId` (uuid del proyecto)

**Respuesta exitosa (200):**
```json
[
  {
    "id": "uuid-decision-1",
    "title": "Migrar de MySQL a PostgreSQL",
    "description": "Se necesita soporte para tipos de datos JSON avanzados",
    "alternatives": ["Mantener MySQL", "Migrar a PostgreSQL", "Migrar a MongoDB"],
    "proposedBy": "uuid-del-usuario",
    "createdAt": "2026-06-20T14:30:00Z"
  }
]
```

**Respuesta de error (404):**
```json
{
  "error": "Proyecto no encontrado"
}
```

---

### POST `/decisions`

**Headers requeridos:** `Authorization: Bearer <token>`

**Body esperado:**
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
{
  "id": "uuid-decision-1",
  "projectId": "uuid-proyecto-1",
  "title": "Migrar de MySQL a PostgreSQL",
  "createdAt": "2026-06-20T14:30:00Z"
}
```

**Respuesta de error (400):**
```json
{
  "error": "El título y la descripción son obligatorios"
}
```

---

### POST `/votes`

**Headers requeridos:** `Authorization: Bearer <token>`

**Body esperado:**
```json
{
  "decisionId": "uuid-decision-1",
  "vote": "approve"
}
```
`vote` acepta los valores `"approve"` o `"reject"`.

**Respuesta exitosa (201):**
```json
{
  "decisionId": "uuid-decision-1",
  "userId": "uuid-del-usuario",
  "vote": "approve"
}
```

**Respuesta de error (409):**
```json
{
  "error": "El usuario ya votó en esta decisión"
}
```

---

### POST `/ai/query`

**Headers requeridos:** `Authorization: Bearer <token>`

**Body esperado:**
```json
{
  "projectId": "uuid-proyecto-1",
  "question": "¿Por qué se migró de MySQL a PostgreSQL?"
}
```

**Respuesta exitosa (200):**
```json
{
  "answer": "Se migró de MySQL a PostgreSQL porque el equipo necesitaba soporte avanzado para tipos de datos JSON. Esta decisión fue propuesta por Vanessa el 20 de junio de 2026, considerando también MongoDB como alternativa."
}
```

**Respuesta de error (500):**
```json
{
  "error": "No se pudo procesar la consulta de IA en este momento"
}
```

## 3. Notas generales

- Todas las rutas que requieren autenticación esperan el header `Authorization: Bearer <token>`, donde `<token>` es el JWT obtenido en `/auth/login`.
- Los errores siempre se devuelven con la forma `{ "error": "mensaje" }`.
- Las fechas se devuelven en formato ISO 8601 (`YYYY-MM-DDTHH:mm:ssZ`).
- Este contrato cubre el alcance mínimo del MVP; endpoints adicionales (como edición o eliminación de decisiones) se documentarán conforme se implementen.
