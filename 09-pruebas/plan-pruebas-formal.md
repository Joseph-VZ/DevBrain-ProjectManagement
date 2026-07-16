# 7. Plan de Pruebas Formal

## 7.1 Estrategia de pruebas

Para validar el correcto funcionamiento del sistema se realizaron pruebas manuales sobre el Producto Mínimo Viable (MVP). Se verificó el funcionamiento de los endpoints del backend mediante **Postman**, comprobando los códigos de respuesta HTTP, la estructura de las respuestas JSON y las reglas de negocio implementadas.

Posteriormente se realizaron pruebas funcionales de la interfaz web utilizando un navegador (**Google Chrome**), validando el flujo de autenticación, la navegación entre módulos, la creación de proyectos, el registro de decisiones, el proceso de votación y la integración con el servicio de inteligencia artificial (**Gemini**).

Las pruebas se enfocaron en validar tanto escenarios exitosos como escenarios de error, verificando que el sistema respondiera con los códigos HTTP adecuados y mostrara mensajes apropiados al usuario.

Las herramientas utilizadas durante el proceso de pruebas fueron:

| Herramienta | Descripción |
|---          |---          |
| Postman     | Pruebas manuales de endpoints del backend y validación de respuestas HTTP. |
| Google Chrome | Pruebas funcionales de la interfaz de usuario. |
| Consola del navegador | Revisión de errores frontend, peticiones y respuestas del sistema. |

---

# 7.2 Casos de prueba — Autenticación

| ID | Descripción | Entrada | Resultado esperado | Resultado real | Estado |
|---|---|---|---|---|---|
| CP-01 | Registro exitoso | Email y contraseña válidos | 201 Created | Se registró el usuario correctamente y el servidor respondió con código 201. | ✅ |
| CP-02 | Email duplicado | Email ya registrado | 400 — email duplicado | El sistema detectó que el correo ya estaba registrado y devolvió un error 400 indicando que el usuario ya existe. | ✅ |
| CP-03 | Login exitoso | Credenciales correctas | 200 + JWT | Se autenticó correctamente y se recibió un token JWT válido. | ✅ |
| CP-04 | Contraseña incorrecta | Password inválido | 401 — credenciales inválidas | El sistema rechazó las credenciales y devolvió un código 401. | ✅ |
| CP-05 | Ruta protegida sin token | Request sin Authorization | 401 — token inválido | El acceso fue denegado debido a la ausencia del token JWT. | ✅ |

**Tabla 17. Casos de prueba del módulo de autenticación.**

---

# 7.3 Casos de prueba — Proyectos, decisiones, votación e IA

| ID | Descripción | Entrada | Resultado esperado | Resultado real | Estado |
|---|---|---|---|---|---|
| CP-06 | Crear proyecto | Nombre y descripción válidos | 201 + proyecto creado | El proyecto fue almacenado correctamente en la base de datos y se devolvió un código 201. | ✅ |
| CP-07 | Listar proyectos | Token válido | 200 + array de proyectos | Se obtuvo correctamente la lista de proyectos registrados. | ✅ |
| CP-08 | Registrar decisión | Campos obligatorios completos | 201 + decisión creada | La decisión fue registrada correctamente y quedó asociada al proyecto correspondiente. | ✅ |
| CP-09 | Votar en decisión | decisionId + vote válido | 201 + voto registrado | El voto se almacenó correctamente y fue asociado al usuario autenticado. | ✅ |
| CP-10 | Voto duplicado | Mismo usuario vota dos veces | 409 — ya votó | El sistema impidió registrar un segundo voto del mismo usuario sobre la misma decisión. | ✅ |
| CP-11 | Consulta IA | Pregunta en lenguaje natural | 200 + respuesta de Gemini | La API respondió correctamente con una recomendación generada mediante Gemini. | ✅ |

**Tabla 18. Casos de prueba de proyectos, decisiones, votación e IA.**

---

# 7.4 Casos de prueba — Flujo de usuario (UI)

| ID | Descripción | Pasos | Resultado esperado | Estado |
|---|---|---|---|---|
| CP-12 | Login desde navegador | 1. Ir a `/login` <br> 2. Ingresar credenciales <br> 3. Presionar Submit | Redirige a `/dashboard` | ✅ |
| CP-13 | Crear proyecto desde UI | 1. Dashboard <br> 2. Seleccionar "Nuevo proyecto" <br> 3. Llenar formulario <br> 4. Guardar | El proyecto aparece en la lista de proyectos | ✅ |
| CP-14 | Sesión persiste | 1. Iniciar sesión <br> 2. Recargar página | La sesión continúa activa | ✅ |
| CP-15 | Ruta protegida sin sesión | 1. Sin iniciar sesión <br> 2. Intentar acceder a `/dashboard` | El usuario es redirigido a `/login` | ✅ |

---

# 7.5 Cobertura de pruebas

La cobertura de pruebas realizada corresponde al **100% de las funcionalidades principales definidas para el MVP**.

Los módulos evaluados fueron:

| Módulo | Casos probados | Cobertura |
|---|---|---|
| Autenticación | CP-01 a CP-05 | 100% |
| Proyectos | CP-06 a CP-07 | 100% |
| Decisiones | CP-08 | 100% |
| Votación | CP-09 a CP-10 | 100% |
| Inteligencia Artificial | CP-11 | 100% |
| Interfaz de usuario | CP-12 a CP-15 | 100% |

En total se realizaron **15 casos de prueba**, incluyendo escenarios exitosos y escenarios de validación de errores, permitiendo comprobar la funcionalidad general del MVP.

---

# 7.6 Referencia a reportes de pruebas existentes

Los reportes y evidencias adicionales de las pruebas realizadas se encuentran dentro de la carpeta:
09-pruebas
