# Smoke Test en Producción

## Objetivo

Validar el funcionamiento del sistema DevBrain desplegado en producción utilizando:

- Frontend: Vercel
- Backend: Render
- Base de datos: Supabase

---

## Flujo probado

| Paso | Resultado |
|-------|-----------|
| Login | ✅ Correcto |
| Crear proyecto | ✅ Correcto |
| Registrar decisión | ✅ Correcto |
| Votar | ✅ Correcto |
| Consultar IA | ✅ Correcto |

---

## Validación del JWT

Se verificó mediante las herramientas de desarrollador del navegador que todas las solicitudes protegidas enviaron correctamente el encabezado:

```
Authorization: Bearer <JWT>
```

Resultado:

✅ Token enviado correctamente.

---

## Diferencias entre producción y local

No se encontraron diferencias funcionales entre el entorno local y el entorno de producción.

---

## Resultado

El flujo completo del sistema fue ejecutado correctamente en producción.

No se detectaron errores críticos que impidan el funcionamiento del MVP.