# Pruebas Sprint 3 - Integración End-to-End

## Información de prueba

**Módulos probados:**
- Autenticación
- Proyectos
- Decisiones
- Votaciones
- Inteligencia Artificial

**Entorno:**
Local

**Fecha:**
07/09/2026

**Responsable:**
Adolfo Montes Zayas

---

# Flujo completo probado

## 1. Login

### Pasos:
1. Abrir la aplicación.
2. Ingresar credenciales válidas.
3. Enviar formulario de inicio de sesión.

### Resultado esperado:
El usuario debe autenticarse correctamente y recibir un token JWT para realizar peticiones protegidas al backend.

### Resultado obtenido:
✅ Correcto

### Validación JWT:
- Token generado correctamente.
- Token enviado en las peticiones posteriores.
- Backend valida correctamente la sesión del usuario.

---

# 2. Crear proyecto

### Pasos:
1. Acceder al dashboard.
2. Seleccionar "Nuevo proyecto".
3. Registrar nombre y descripción.
4. Guardar proyecto.

### Resultado esperado:
El proyecto debe crearse correctamente, almacenarse en la base de datos y aparecer disponible en el listado de proyectos del usuario.

### Resultado obtenido:
✅ Correcto

---

# 3. Registrar decisión

### Pasos:
1. Entrar al proyecto creado.
2. Acceder al módulo de decisiones.
3. Crear una nueva decisión.
4. Completar título, descripción y alternativas.
5. Guardar información.

### Datos utilizados:

**Título:**
Selección de base de datos

**Descripción:**
Se requiere seleccionar una base de datos adecuada para el almacenamiento de información del sistema.

**Alternativas:**
- PostgreSQL
- MySQL

### Resultado esperado:
La decisión debe almacenarse correctamente, estar asociada al proyecto seleccionado y estar disponible para consulta y votación.

### Resultado obtenido:
✅ Correcto

---

# 4. Votar decisión

### Pasos:
1. Abrir la decisión creada.
2. Seleccionar una alternativa.
3. Confirmar el voto.

### Resultado esperado:
El voto debe registrarse correctamente, actualizar el contador de votos y reflejar la selección realizada por el usuario.

### Resultado obtenido:
❌ Falló

### Descripción del problema:
El módulo de decisiones no permite completar correctamente el flujo de votación debido a que la sección de decisiones no carga la información necesaria, impidiendo continuar con la interacción de voto.

---

# 5. Consulta IA

### Pasos:
1. Acceder al chat de DevBrain IA.
2. Seleccionar el proyecto creado.
3. Realizar una pregunta relacionada con la decisión registrada.
4. Esperar respuesta de Gemini.

### Pregunta realizada:

"Describe la decisión creada en este proyecto."

### Resultado esperado:
La IA debe responder utilizando el contexto real de las decisiones almacenadas en el proyecto.

### Resultado obtenido:
✅ Correcto

### Respuesta obtenida:
La IA respondió utilizando la información disponible de la decisión registrada en el proyecto.

---

# Verificación Frontend - Backend

## JWT

Validación:

- Login genera token correctamente.
- Token enviado en las solicitudes protegidas.
- Backend valida correctamente la identidad del usuario.

Resultado:

✅ Correcto

---


# Inconsistencias encontradas

## Bug 1

**Título:**
No se permite completar el flujo de votación de decisiones.

**Descripción:**
El apartado de decisiones no carga correctamente la información, por lo que no es posible acceder a la decisión creada para realizar una votación.

**Pasos para reproducir:**

1. Iniciar sesión con un usuario válido.
2. Acceder al dashboard de proyectos.
3. Seleccionar un proyecto existente.
4. Intentar ingresar al apartado de decisiones.
5. Esperar la carga de la información.
6. Verificar que la pantalla permanece cargando y no muestra las decisiones disponibles.
7. Intentar realizar una votación.

**Resultado esperado:**
El sistema debe mostrar las decisiones del proyecto y permitir seleccionar una alternativa para registrar un voto.

**Resultado obtenido:**
La pantalla de decisiones permanece en estado de carga, impidiendo acceder a la decisión y realizar la votación.

**Estado:**
Pendiente

---


---

# Conclusión

El flujo completo de integración fue probado:

✅ Login  
✅ Creación de proyecto  
✅ Registro de decisión  
❌ Votación  
✅ Consulta IA  

Resultado general:

La integración entre frontend y backend funciona correctamente en los módulos de autenticación, proyectos, decisiones e inteligencia artificial.

Se identificó un problema en el flujo de votación que impide completar la interacción con las decisiones debido a un error de carga en el módulo correspondiente. El bug quedó documentado con pasos claros de reproducción.