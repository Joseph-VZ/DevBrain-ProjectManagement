


UNIVERSIDAD TECNOLÓGICA DE PUEBLA
DIVISIÓN DE TECNOLOGÍAS DE LA INFORMACIÓN
INGENIERÍA EN DESARROLLO Y 
GESTIÓN DE SOFTWARE
ASIGNATURA:
ADMINISTRACIÓN DE PROYECTOS PARA TI
ACTIVIDAD:
LECCIONES APRENDIDAS
INTEGRANTES DEL EQUIPO:
CARRERA JIMÉNEZ AMÉRICA
GARCÍA VÁZQUEZ VANESSA KRYSTAL
JUÁREZ LÓPEZ JESÚS
LUCERO VÁZQUEZ JOSEPH
MONTES ZAYAS ADOLFO
NOMBRE DEL PROFESOR:
HERNÁNDEZ SALAS CARLOS FEDERICO 
CUATRIMESTRE:
MAYO – AGOSTO 2026
GRUPO:
9°C

# ÍNDICE

LECCIONES APRENDIDAS – DEVBRAIN	3

1.1 Introducción	3

1.2 Lecciones Técnicas	3
1.2.1 Mantener una estrategia clara de ramas y control de versiones	3
1.2.2 Utilizar convenciones de commits	3
1.2.3 Mantener una estructura organizada del proyecto	3
1.2.4 Realizar integración continua entre frontend y backend	4
1.2.5 Realizar pruebas de endpoints antes de integrar funcionalidades	4
1.2.6 Uso de Supabase como plataforma de datos y servicios backend	4
1.2.7 Integración de inteligencia artificial mediante Gemini	5

1.3 Lecciones de Gestión del Proyecto	5
1.3.1 Mantener comunicación constante entre integrantes	5
1.3.2 Dar seguimiento mediante GitHub Projects	5
1.3.3 Mejorar la coordinación durante los sprints	6

1.4 Lecciones de Documentación	6
1.4.1 Documentar durante todo el desarrollo	6

1.5 Recomendaciones para proyectos futuros	7

1.6 Conclusión	7

 # LECCIONES APRENDIDAS – DEVBRAIN

## 1.1 Introducción

Durante el desarrollo del proyecto DevBrain se presentaron diferentes retos relacionados con la organización del equipo, control de versiones, desarrollo de funcionalidades, integración de tecnologías y documentación.

Estas experiencias permitieron identificar prácticas que funcionaron correctamente, problemas encontrados durante el proceso y mejoras que pueden aplicarse en futuros proyectos.

Cada lección se describe mediante la estructura:

**Situación → Impacto → Qué haríamos diferente**

---

# 1.2 Lecciones Técnicas

## 1.2.1 Mantener una estrategia clara de ramas y control de versiones

**Situación:**  
Durante el desarrollo del proyecto se utilizó Git y GitHub como herramientas principales para administrar los cambios realizados por los integrantes del equipo, trabajando con ramas independientes para desarrollar funcionalidades específicas.

**Impacto:**  
El uso de ramas permitió separar los cambios de cada funcionalidad y facilitó la integración del trabajo realizado por diferentes miembros del equipo.

**Qué haríamos diferente:**  
Definir desde el inicio una estrategia de ramas más detallada, estableciendo reglas claras para creación de ramas, integración de cambios y manejo de versiones.

---

## 1.2.2 Utilizar convenciones de commits

**Situación:**  
El equipo utilizó convenciones de commits para identificar el propósito de cada modificación realizada en el repositorio, utilizando etiquetas como `feat`, `fix`, `docs` y `chore`.

**Impacto:**  
Esto permitió mantener un historial de cambios más ordenado y facilitó identificar rápidamente qué funcionalidad o corrección había sido realizada.

**Qué haríamos diferente:**  
Establecer las convenciones de commits como una regla desde el inicio del proyecto para que todos los integrantes mantengan el mismo formato.

---

## 1.2.3 Mantener una estructura organizada del proyecto

**Situación:**  
El proyecto fue desarrollado separando responsabilidades entre frontend y backend, utilizando tecnologías diferentes para cada parte del sistema.

**Impacto:**  
La organización permitió trabajar los módulos de manera independiente y facilitó el mantenimiento del código durante el desarrollo.

**Qué haríamos diferente:**  
Definir desde la primera etapa una estructura completa del proyecto, documentando la función de cada carpeta, módulo y componente.

---

## 1.2.4 Realizar integración continua entre frontend y backend

**Situación:**  
Durante el desarrollo fue necesario conectar constantemente la interfaz web con los servicios del backend para validar el funcionamiento de los módulos implementados.

**Impacto:**  
Las pruebas de integración permitieron detectar problemas relacionados con comunicación entre servicios, envío de datos y respuestas de la API.

**Qué haríamos diferente:**  
Realizar integraciones más frecuentes después de terminar cada funcionalidad para identificar errores antes de continuar con nuevos módulos.

---

## 1.2.5 Realizar pruebas de endpoints antes de integrar funcionalidades

**Situación:**  
Se utilizaron herramientas como Postman para probar los endpoints del sistema, verificando respuestas del servidor, códigos HTTP y comportamiento esperado de cada servicio.

**Impacto:**  
Esto permitió comprobar el correcto funcionamiento del backend antes de realizar la conexión con la interfaz del usuario.

**Qué haríamos diferente:**  
Crear casos de prueba desde el desarrollo inicial de cada endpoint y mantener una documentación actualizada de los resultados obtenidos.

---

## 1.2.6 Uso de Supabase como plataforma de datos y servicios backend

**Situación:**  
Durante el desarrollo del proyecto se utilizó Supabase para la administración de información del sistema, manejo de usuarios y almacenamiento de datos necesarios para las funcionalidades del proyecto.

**Impacto:**  
El uso de Supabase permitió agilizar el desarrollo al contar con servicios integrados y reducir la necesidad de configurar infraestructura desde cero. Sin embargo, fue necesario comprender correctamente la estructura de datos, relaciones y configuración de acceso.

**Qué haríamos diferente:**  
Realizar desde las primeras etapas una planificación más detallada de la estructura de datos, permisos y relaciones antes de iniciar el desarrollo de los módulos principales.

---

## 1.2.7 Integración de inteligencia artificial mediante Gemini

**Situación:**  
El proyecto incorporó Gemini como servicio de inteligencia artificial para generar respuestas y apoyar funcionalidades relacionadas con consultas dentro del sistema.

**Impacto:**  
La integración permitió agregar una funcionalidad avanzada al proyecto, aunque fue necesario considerar validaciones, manejo de errores y respuestas generadas por un servicio externo.

**Qué haríamos diferente:**  
Realizar pruebas tempranas con diferentes tipos de consultas y establecer reglas más específicas para controlar las respuestas generadas por la inteligencia artificial.

---

# 1.3 Lecciones de Gestión del Proyecto

## 1.3.1 Mantener comunicación constante entre integrantes

**Situación:**  
El equipo mantuvo comunicación durante el desarrollo para compartir avances, resolver dudas y coordinar las actividades asignadas.

**Impacto:**  
La comunicación permitió continuar con el avance del proyecto y resolver problemas encontrados durante cada etapa.

**Qué haríamos diferente:**  
Establecer reuniones breves de seguimiento con mayor frecuencia para revisar avances, bloqueos y pendientes de cada integrante.

---

## 1.3.2 Dar seguimiento mediante GitHub Projects

**Situación:**  
Se utilizó GitHub Projects como tablero de organización para administrar tareas, visualizar avances y distribuir actividades durante los sprints.

**Impacto:**  
El tablero permitió tener una visión general del estado del proyecto y facilitó identificar tareas pendientes o en proceso.

**Qué haríamos diferente:**  
Actualizar el tablero después de cada avance importante para mantener siempre información actualizada sobre el progreso.

---

## 1.3.3 Mejorar la coordinación durante los sprints

**Situación:**  
Durante algunos momentos del desarrollo fue necesario reorganizar actividades para cumplir con los objetivos establecidos dentro del tiempo disponible.

**Impacto:**  
La distribución de tareas tuvo que ajustarse para mantener el avance del proyecto y completar las funcionalidades necesarias.

**Qué haríamos diferente:**  
Realizar una planeación más detallada al inicio de cada sprint, considerando tiempos estimados, dependencias y posibles riesgos.

---

# 1.4 Lecciones de Documentación

## 1.4.1 Documentar durante todo el desarrollo

**Situación:**  
Algunas evidencias, reportes y documentos del proyecto fueron recopilados durante las etapas finales del desarrollo.

**Impacto:**  
Esto generó una mayor carga de trabajo al momento de preparar la entrega final, debido a que fue necesario organizar información de actividades realizadas anteriormente.

**Qué haríamos diferente:**  
Crear documentación progresiva durante cada sprint, registrando avances, decisiones técnicas, pruebas y evidencias desde el inicio.

---

# 1.5 Recomendaciones para proyectos futuros

- Definir una estrategia de Git y ramas antes de iniciar el desarrollo.
- Mantener actualizado el tablero de gestión del proyecto.
- Realizar pruebas desde la creación de cada funcionalidad.
- Documentar avances durante todo el ciclo de desarrollo.
- Establecer reglas claras de comunicación entre integrantes.
- Realizar integraciones frecuentes entre frontend y backend.
- Planificar la estructura de datos antes de comenzar la implementación.
- Registrar las decisiones técnicas importantes del proyecto.

---

# 1.6 Conclusión

El desarrollo de DevBrain permitió al equipo identificar la importancia de la organización, comunicación y aplicación de buenas prácticas durante un proyecto de software.

Las experiencias obtenidas ayudaron a comprender que una correcta planificación, pruebas constantes, documentación continua y coordinación entre integrantes son factores fundamentales para lograr un desarrollo más eficiente.

Las lecciones aprendidas servirán como base para mejorar la ejecución de futuros proyectos, aplicando mejores estrategias de trabajo y tomando decisiones técnicas más estructuradas.