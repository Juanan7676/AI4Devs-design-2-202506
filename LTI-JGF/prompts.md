Modelo usado: Claude-4-sonnet

# Prompt 1: Generación de user stories

```Dado el PRD del ATS de LTI definido en @LTI-JGF.md, define las principales historias de usuario.

Para generarlas, usa la siguiente plantilla:

[Título de la Historia de Usuario]: 

    Como [rol del usuario],
    quiero [acción que desea realizar el usuario],
    para que [beneficio que espera obtener el usuario].

Criterios de Aceptación:

    [Detalle específico de funcionalidad]
    [Detalle específico de funcionalidad]
    [Detalle específico de funcionalidad]

Notas Adicionales:

    [Cualquier consideración adicional]

Historias de Usuario Relacionadas:

    [Relaciones con otras historias de usuario]
```
Por qué este prompt es bueno:

    - Da el contexto adecuado (artefactos generados en el ejercicio anterior)
    - Especifica el formato de respuesta deseado (plantilla)
    - Limita el número de historias de usuario a 5 (si no le especificaba un máximo, generaba 20 historias lo cual hacía todo un poco inmanejable)

# Prompt 2: Priorización de historias de usuario
```
Considera ahora el backlog que has creado con las diferentes historias de usuario. Quiero que estimes para cada historia:
    Impacto en el usuario y valor del negocio.
    Urgencia basada en tendencias del mercado y feedback de usuarios.
    Complejidad y esfuerzo estimado de implementación.
    Riesgos y dependencias entre tareas.

Para ello, genera una tabla markdown en otra sección del archivo @UserStories-JGF.md  en el que las historias de usuario estén ordenadas por prioridad, y en cada columna pongas la valoración que le has dado en la historia de usuario (Baja, Media, Alta) en cada apartado.
```
Por qué este prompt fue bueno:
```
- Le da el contexto adecuado (volví a adjuntar el PRD y el mismo documento UserStories-JGF.md en el que escribió anteriormente)
- Especifica claramente la metodología para estimar la prioridad
- Especifica el formato de salida (tabla markdown, cómo ordenar las filas y qué información mostrar en las columnas)
```
# Prompt 3: Generación de tickets de trabajo
```
Ahora, para la historia de usuario 1 (la primera), quiero que generes los tickets de trabajo necesarios para completar los criterios de aceptación que se detallan en ella. Para cada ticket de trabajo, sigue la siguiente plantilla:

Título: [Título de la tarea]
Descripción: [Detalla aquí el propósito (por qué es necesaria la tarea y qué problema resuelve) y los detalles específicos (información adicional sobre requerimientos específicos, restricciones, o condiciones necesarias para la realización de la tarea)]
Criterios de Aceptación:
  - [Criterio 1]
  - [Criterio 2]
  - ...
[Se trata de una lista detallada de condiciones que deben cumplirse para que el trabajo en el ticket se considere completado. Incluye pasos o pruebas específicas que se deben realizar para verificar que la tarea se ha completado correctamente.]
Prioridad: [Detalla aquí el nivel de urgencia del ticket con respecto a los demás tickets de esta historia de usuario]
Estimación: [Haz una estimación del esfuerzo que requiere la tarea, medida en puntos de historia y siguiendo el sistema de fibonacci]
Asignado a: [Responsable de la tarea. Puede ser Equipo de Backend, Equipo de Frontend, Equipo de Diseño]
Etiquetas: [Pon aquí las etiquetas asignadas a este ticket. Por ejemplo: "UI" "Backend" "Seguridad" "Base de datos"]
Comentarios: [De momento, deja vacío este apartado]
Enlaces: [De momento, deja vacío este apartado]
Historial de Cambios: [De momento, deja vacío este apartado]
```
Por qué este prompt fue bueno:
```
- Vuelve a dar el contexto adecuado al asistente
- Da un formato de salida específico mediante una plantilla, y detalla pormenorizadamente qué debe rellenarse en cada apartado
```