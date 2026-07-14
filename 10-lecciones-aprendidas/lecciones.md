


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

ÍNDICE
LECCIONES APRENDIDAS – DEVBRAIN	3
1.1 Introducción	3
1.2 Lecciones Técnicas	3
1.2.1 Mantener una estrategia clara de ramas	3
1.2.2. Mantener una estructura consistente del proyecto	3
1.2.3. Utilizar convenciones de commits	3
1.2.4. Documentar la API conforme se desarrolla	3
1.2.5. Integración continua entre frontend y backend	4
1.3 Lecciones de Gestión	4
1.3.1 Distribuir la carga de trabajo de forma equilibrada	4
1.3.2 Mantener comunicación constante	4
1.3.3 Dar seguimiento mediante GitHub Projects	4
1.4 Recomendaciones para Proyectos Futuros	5
1.5 Conclusión	5

 
LECCIONES APRENDIDAS – DEVBRAIN
1.1 Introducción
Durante el desarrollo de DevBrain surgieron distintos retos tanto técnicos como de organización. A partir de ellos, el equipo identificó varias prácticas que funcionaron correctamente y otras que pueden mejorarse en futuros proyectos.
1.2 Lecciones Técnicas
1.2.1 Mantener una estrategia clara de ramas
En algunos momentos del proyecto se realizaron Pull Requests hacia la rama main en lugar de develop, lo que provocó trabajo adicional para sincronizar los cambios.
Lección: Definir desde el inicio una estrategia de ramas y asegurarse de que todos los integrantes la comprendan y la respeten.

1.2.2. Mantener una estructura consistente del proyecto
Se detectaron archivos duplicados en el backend, como controladores y rutas con nombres similares, lo que generó confusión durante el desarrollo.
Lección: Revisar periódicamente la estructura del proyecto para eliminar archivos obsoletos y evitar duplicidad de código.

1.2.3. Utilizar convenciones de commits
El uso de convenciones como feat, fix, docs, refactor y test facilitó la comprensión del historial de cambios y permitió identificar rápidamente el propósito de cada modificación.
Lección: Mantener una convención de commits desde el inicio mejora la trazabilidad del proyecto.

1.2.4. Documentar la API conforme se desarrolla
Actualizar el contrato de la API al mismo tiempo que se implementan los endpoints evita inconsistencias entre frontend y backend.
Lección: La documentación debe mantenerse sincronizada con el desarrollo y no dejarse únicamente para la etapa final.

1.2.5. Integración continua entre frontend y backend
Realizar pruebas de integración de forma constante permitió detectar incompatibilidades antes de la entrega final.
Lección: Integrar los módulos de manera frecuente reduce errores y facilita la detección temprana de problemas.

1.3 Lecciones de Gestión
1.3.1 Distribuir la carga de trabajo de forma equilibrada
Durante algunos sprints fue necesario que integrantes del equipo apoyaran en áreas distintas a su responsabilidad principal para cumplir con los objetivos.
Lección: Una distribución flexible del trabajo permite mantener el avance del proyecto cuando surgen imprevistos.

1.3.2 Mantener comunicación constante
Las reuniones periódicas y la comunicación continua facilitaron la resolución de dudas y el seguimiento de las tareas asignadas.
Lección: Una comunicación clara reduce retrasos y mejora la coordinación del equipo.

1.3.3 Dar seguimiento mediante GitHub Projects
El tablero de GitHub permitió conocer el estado de cada actividad y visualizar el progreso del sprint.
Lección: Actualizar constantemente el tablero facilita la organización y el seguimiento de las tareas.

 
1.4 Recomendaciones para Proyectos Futuros
•	Definir desde el inicio las reglas para el uso de ramas y Pull Requests.
•	Mantener actualizada la documentación técnica durante todo el desarrollo.
•	Realizar revisiones de código antes de aprobar cada Pull Request.
•	Integrar y probar frontend y backend de manera continua, evitando dejar la integración para las últimas etapas.
•	Planificar reuniones de seguimiento semanales para revisar avances, resolver bloqueos y redistribuir tareas cuando sea necesario.
1.5 Conclusión
La realización de este proyecto permitió al equipo conocer la importancia de mantener una buena comunicación, seguir una organización clara y documentar adecuadamente cada etapa del desarrollo. La experiencia obtenida ayudará a afrontar futuros proyectos con una mejor planificación y coordinación.
