# Investigación del Problema y Objetivos — DevBrain

## 1. Contexto

En el desarrollo de software, los equipos toman constantemente decisiones técnicas importantes: qué tecnología usar, cómo resolver un problema de arquitectura, por qué migrar de una herramienta a otra, qué alternativa se descartó y por qué. Estas decisiones definen el rumbo del proyecto, pero rara vez quedan documentadas de forma estructurada y consultable.

## 2. El problema

Las herramientas tradicionales de gestión de proyectos (Jira, Trello, Asana, GitHub Projects, etc.) están diseñadas para responder **qué se hizo** y **cuándo**: tareas, estados, fechas de entrega. Sin embargo, ninguna de ellas responde de forma estructurada a una pregunta igual de importante: **¿por qué se hizo así?**

Con el tiempo, esto genera varios problemas recurrentes en los equipos de desarrollo:

- Se pierde el razonamiento detrás de decisiones clave (por ejemplo, por qué se migró de MySQL a PostgreSQL)
- Nuevos integrantes del equipo no tienen forma de entender el contexto histórico de las decisiones ya tomadas
- Se repiten discusiones sobre alternativas que ya fueron evaluadas y descartadas anteriormente
- No queda claro quién propuso una decisión ni quiénes participaron en su evaluación
- El conocimiento técnico vive de forma dispersa: en chats, correos, o simplemente en la memoria de quien estuvo presente

Este problema se vuelve más crítico en proyectos largos, con rotación de personal, o en equipos académicos donde la documentación del proceso de decisión es tan importante como el resultado final.

## 3. Propuesta de solución: DevBrain

DevBrain es una plataforma enfocada en la **gestión del conocimiento técnico** dentro de proyectos de software. A diferencia de las herramientas tradicionales, su propósito central es registrar, organizar y consultar el historial de decisiones importantes tomadas durante el desarrollo de un proyecto.

Permite responder preguntas como:

- ¿Por qué se tomó esta decisión técnica?
- ¿Quién la propuso?
- ¿Qué alternativas se evaluaron antes de llegar a esta?
- ¿Quiénes participaron en la discusión y votación?

Además, DevBrain incorpora una capa de inteligencia artificial (Gemini API) capaz de responder preguntas en lenguaje natural utilizando el historial de decisiones registradas como contexto, sin que el usuario tenga que buscar manualmente entre los registros.

## 4. Objetivo general

Desarrollar una plataforma web funcional que permita a equipos de desarrollo de software registrar, consultar y analizar sus decisiones técnicas a lo largo de un proyecto, facilitando la trazabilidad del conocimiento y el razonamiento detrás de cada decisión.

## 5. Objetivos específicos

1. Permitir el registro estructurado de decisiones técnicas, incluyendo contexto, alternativas evaluadas y participantes
2. Implementar un sistema de votación que permita al equipo expresar consenso o desacuerdo sobre una decisión propuesta
3. Construir una línea de tiempo (timeline) que muestre la evolución cronológica de las decisiones de un proyecto
4. Integrar un asistente de IA capaz de responder preguntas sobre el historial de decisiones utilizando el contexto real registrado en la plataforma
5. Garantizar autenticación segura de usuarios mediante JWT y una gestión de proyectos que permita organizar las decisiones por equipo o iniciativa
6. Entregar una API REST documentada y una base de datos relacional que soporte el modelo de datos del sistema

## 6. Justificación

Este proyecto es relevante tanto desde una perspectiva práctica como académica: resuelve un vacío real en las herramientas de gestión de proyectos existentes, y permite aplicar de forma integral los conocimientos de la materia de Administración de Proyectos para TI — gestión de equipos, control de versiones, metodologías ágiles y documentación profesional — sobre un producto de software funcional.
