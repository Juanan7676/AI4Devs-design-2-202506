# Historias de Usuario Principales - TalentFlow ATS

## 1. [Crear y Publicar Oferta de Empleo]

    Como reclutador,
    quiero crear una nueva oferta de empleo y publicarla automáticamente en portales de empleo,
    para que pueda difundir la vacante de manera eficiente y comenzar a recibir candidaturas.

Criterios de Aceptación:

    - El sistema debe permitir crear ofertas con título, descripción, ubicación y requisitos
    - Debe incluir campos para configurar etapas personalizadas del proceso de selección
    - La oferta se debe publicar automáticamente en portales conectados (LinkedIn, InfoJobs, etc.)
    - El sistema debe generar un enlace único para candidaturas directas
    - Se debe mostrar el estado de publicación en tiempo real

Notas Adicionales:

    - Considerar integración con múltiples portales de empleo
    - Permitir guardar plantillas de ofertas para reutilización
    - Incluir validación de campos obligatorios

Historias de Usuario Relacionadas:

    - [Gestión del Pipeline de Candidatos]
    - [Recepción y Procesamiento de Candidaturas]

---

## 2. [Recepción y Procesamiento Automático de Candidaturas]

    Como reclutador,
    quiero que las candidaturas se procesen automáticamente y se extraiga información clave de los CVs,
    para que pueda evaluar rápidamente a los candidatos sin trabajo manual de cribado inicial.

Criterios de Aceptación:

    - El sistema debe recibir candidaturas desde portales de empleo y formulario directo
    - Debe extraer automáticamente: nombre, email, teléfono, experiencia, formación y habilidades
    - Debe crear un perfil estructurado del candidato con la información extraída
    - Los CVs se deben almacenar de forma segura y accesible
    - Se debe notificar al reclutador de nuevas candidaturas con resumen del perfil

Notas Adicionales:

    - Implementar parsing inteligente de diferentes formatos de CV (PDF, Word, etc.)
    - Considerar integración con LinkedIn para enriquecer perfiles
    - Incluir validación de datos extraídos

Historias de Usuario Relacionadas:

    - [Crear y Publicar Oferta de Empleo]
    - [Gestión del Pipeline de Candidatos]

---

## 3. [Gestión del Pipeline de Candidatos]

    Como reclutador,
    quiero visualizar y gestionar candidatos en un pipeline visual tipo Kanban,
    para que pueda tener visibilidad clara del estado de cada candidato y tomar decisiones colaborativas.

Criterios de Aceptación:

    - Mostrar candidatos organizados por etapas configurables del proceso
    - Permitir arrastrar y soltar candidatos entre etapas
    - Mostrar información clave del candidato en cada tarjeta (nombre, experiencia, estado)
    - Permitir agregar comentarios internos y asignar responsables
    - Debe soportar múltiples ofertas simultáneamente con filtros

Notas Adicionales:

    - Implementar notificaciones automáticas al cambiar de etapa
    - Considerar automatizaciones basadas en cambios de etapa
    - Incluir vista de timeline del proceso por candidato

Historias de Usuario Relacionadas:

    - [Recepción y Procesamiento de Candidaturas]
    - [Comunicación con Candidatos]
    - [Programación de Entrevistas]

---

## 4. [Comunicación Integrada con Candidatos]

    Como reclutador,
    quiero enviar emails directamente desde la plataforma usando plantillas predefinidas,
    para que pueda mantener comunicación profesional y eficiente con los candidatos.

Criterios de Aceptación:

    - Enviar emails directamente desde la interfaz del ATS
    - Usar plantillas personalizables para diferentes tipos de comunicación
    - Registrar automáticamente todo el historial de comunicaciones
    - Permitir automatizaciones (ej: email de rechazo al mover a etapa "Descartado")
    - Incluir seguimiento de apertura y respuesta de emails

Notas Adicionales:

    - Integrar con servicios de email (SendGrid, Amazon SES)
    - Considerar programación de emails para horarios óptimos
    - Incluir firma corporativa automática

Historias de Usuario Relacionadas:

    - [Gestión del Pipeline de Candidatos]
    - [Programación de Entrevistas]

---

## 5. [Programación de Entrevistas]

    Como reclutador,
    quiero programar entrevistas e invitar automáticamente a candidatos y entrevistadores,
    para que pueda coordinar el proceso de selección de manera eficiente.

Criterios de Aceptación:

    - Programar entrevistas con fecha, hora, duración y tipo (presencial/online)
    - Integrar con calendarios externos (Google Calendar, Outlook)
    - Enviar invitaciones automáticas a candidatos y entrevistadores
    - Incluir enlaces de videollamada para entrevistas online
    - Permitir agregar notas y preparación para la entrevista
    - Mostrar agenda de entrevistas por candidato y entrevistador

Notas Adicionales:

    - Considerar zonas horarias de candidatos
    - Implementar recordatorios automáticos
    - Incluir feedback post-entrevista

Historias de Usuario Relacionadas:

    - [Gestión del Pipeline de Candidatos]
    - [Comunicación Integrada con Candidatos]

---

# Matriz de Priorización del Backlog

## Tabla de Priorización:

| Prioridad | Historia de Usuario | Impacto | Urgencia | Complejidad | Riesgos | Justificación |
|-----------|-------------------|---------|----------|-------------|---------|---------------|
| **1** | Gestión del Pipeline de Candidatos | **Alta** | **Alta** | Media | Baja | Core del producto, diferenciador clave, fácil implementación |
| **2** | Crear y Publicar Oferta de Empleo | **Alta** | **Alta** | Media | Media | Punto de entrada crítico, dependencia para otras funcionalidades |
| **3** | Recepción y Procesamiento Automático de Candidaturas | **Alta** | Media | **Alta** | **Alta** | Alto valor pero complejo, requiere integraciones externas |
| **4** | Comunicación Integrada con Candidatos | Media | Media | Baja | Media | Funcionalidad complementaria, fácil de implementar |
| **5** | Programación de Entrevistas | Media | Baja | **Alta** | **Alta** | Funcionalidad avanzada, requiere múltiples integraciones |
## Recomendación de Roadmap:

**MVP (Sprint 1-2):**
1. Gestión del Pipeline de Candidatos
2. Crear y Publicar Oferta de Empleo

**V2 (Sprint 3-4):**
3. Recepción y Procesamiento Automático de Candidaturas
4. Comunicación Integrada con Candidatos

**V3 (Sprint 5-6):**
5. Programación de Entrevistas

---

# Tickets de Trabajo - Historia de Usuario 1: Crear y Publicar Oferta de Empleo

## Ticket 1.1: Diseño de la Interfaz de Creación de Ofertas

**Título:** Diseño de la Interfaz de Creación de Ofertas

**Descripción:** Crear el diseño visual y la experiencia de usuario para el formulario de creación de ofertas de empleo. Esta tarea es necesaria para proporcionar una interfaz intuitiva y profesional que permita a los reclutadores crear ofertas de manera eficiente, siguiendo las mejores prácticas de UX/UI para formularios complejos.

**Criterios de Aceptación:**
- El formulario debe incluir todos los campos obligatorios: título, descripción, ubicación, requisitos
- La interfaz debe ser responsive y funcionar correctamente en desktop, tablet y móvil
- El diseño debe seguir el sistema de diseño de TalentFlow (colores, tipografía, componentes)
- Debe incluir validación visual en tiempo real de los campos
- El formulario debe tener un flujo lógico y progresivo
- Debe incluir opciones para guardar como borrador y publicar
- La interfaz debe mostrar claramente el progreso de completado del formulario

**Prioridad:** Alta - Es el punto de entrada del flujo principal

**Estimación:** 8 puntos

**Asignado a:** Equipo de Diseño

**Etiquetas:** UI, UX, Diseño, Frontend

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.2: Implementación del Formulario de Creación de Ofertas

**Título:** Implementación del Formulario de Creación de Ofertas

**Descripción:** Desarrollar el componente React del formulario de creación de ofertas con todas las funcionalidades de validación, manejo de estado y envío de datos. Esta tarea es necesaria para convertir el diseño en una funcionalidad operativa que permita a los usuarios crear ofertas de empleo de manera efectiva.

**Criterios de Aceptación:**
- Implementar todos los campos del formulario con validación en tiempo real
- Manejar el estado del formulario (borrador, envío, éxito, error)
- Implementar validación de campos obligatorios y formatos
- Crear componentes reutilizables para campos de formulario
- Implementar funcionalidad de guardado automático como borrador
- Manejar errores de red y mostrar mensajes apropiados
- Integrar con el sistema de notificaciones para feedback al usuario

**Prioridad:** Alta - Dependencia para otras funcionalidades

**Estimación:** 13 puntos

**Asignado a:** Equipo de Frontend

**Etiquetas:** Frontend, React, Formularios, Validación

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.3: Modelo de Datos y API para Ofertas de Empleo

**Título:** Modelo de Datos y API para Ofertas de Empleo

**Descripción:** Crear el modelo de datos en la base de datos y desarrollar los endpoints de la API REST para gestionar ofertas de empleo. Esta tarea es necesaria para proporcionar la infraestructura de datos que soporte la creación, edición y gestión de ofertas de empleo en el sistema.

**Criterios de Aceptación:**
- Crear tabla JobOffer con todos los campos necesarios (id, title, description, location, requirements, status, etc.)
- Implementar endpoints CRUD para ofertas de empleo (CREATE, READ, UPDATE, DELETE)
- Implementar validación de datos en el backend
- Crear índices apropiados para consultas eficientes
- Implementar soft delete para ofertas
- Añadir campos de auditoría (created_at, updated_at, created_by)
- Documentar la API con OpenAPI/Swagger

**Prioridad:** Alta - Infraestructura crítica del sistema

**Estimación:** 8 puntos

**Asignado a:** Equipo de Backend

**Etiquetas:** Backend, API, Base de datos, Modelo de datos

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.4: Configuración de Etapas Personalizables del Proceso

**Título:** Configuración de Etapas Personalizables del Proceso

**Descripción:** Implementar la funcionalidad para que los usuarios puedan configurar etapas personalizadas del proceso de selección al crear una oferta. Esta tarea es necesaria para proporcionar flexibilidad a diferentes empresas que tienen procesos de selección distintos.

**Criterios de Aceptación:**
- Permitir crear, editar y eliminar etapas personalizadas
- Implementar ordenamiento de etapas mediante drag-and-drop
- Proporcionar etapas por defecto que se puedan personalizar
- Validar que no se puedan eliminar etapas con candidatos asignados
- Permitir configurar colores y nombres personalizados para cada etapa
- Implementar plantillas de etapas predefinidas por industria
- Guardar la configuración de etapas por oferta

**Prioridad:** Media - Funcionalidad diferenciadora pero no crítica para MVP

**Estimación:** 13 puntos

**Asignado a:** Equipo de Frontend + Equipo de Backend

**Etiquetas:** Frontend, Backend, Configuración, Pipeline

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.5: Integración con Portales de Empleo

**Título:** Integración con Portales de Empleo

**Descripción:** Desarrollar las integraciones con portales de empleo externos (LinkedIn, InfoJobs, etc.) para publicar ofertas automáticamente. Esta tarea es necesaria para ampliar el alcance de las ofertas y automatizar el proceso de publicación en múltiples plataformas.

**Criterios de Aceptación:**
- Implementar integración con LinkedIn Jobs API
- Implementar integración con InfoJobs API
- Crear sistema de mapeo de campos entre TalentFlow y portales externos
- Implementar manejo de errores y reintentos automáticos
- Crear dashboard de estado de publicaciones por portal
- Implementar sincronización de estado de ofertas (activa/pausada/cerrada)
- Crear logs detallados de todas las operaciones de publicación

**Prioridad:** Media - Funcionalidad importante pero compleja

**Estimación:** 21 puntos

**Asignado a:** Equipo de Backend

**Etiquetas:** Backend, Integración, APIs externas, Portales de empleo

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.6: Generación de Enlaces Únicos para Candidaturas

**Título:** Generación de Enlaces Únicos para Candidaturas

**Descripción:** Crear un sistema para generar enlaces únicos y seguros para cada oferta de empleo que permita a los candidatos aplicar directamente. Esta tarea es necesaria para proporcionar una forma directa de recibir candidaturas sin depender únicamente de portales externos.

**Criterios de Aceptación:**
- Generar URLs únicas y seguras para cada oferta
- Implementar sistema de tracking de visitas a enlaces
- Crear página de aplicación directa con formulario de candidatura
- Implementar validación de enlaces expirados o inactivos
- Crear sistema de enlaces de seguimiento para analytics
- Implementar rate limiting para prevenir spam
- Añadir opción de desactivar enlaces directos por oferta

**Prioridad:** Media - Funcionalidad complementaria importante

**Estimación:** 8 puntos

**Asignado a:** Equipo de Frontend + Equipo de Backend

**Etiquetas:** Frontend, Backend, Seguridad, URLs, Tracking

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.7: Dashboard de Estado de Publicación en Tiempo Real

**Título:** Dashboard de Estado de Publicación en Tiempo Real

**Descripción:** Crear una interfaz que muestre el estado de publicación de las ofertas en tiempo real, incluyendo estadísticas de visualizaciones y candidaturas recibidas. Esta tarea es necesaria para proporcionar visibilidad y control a los reclutadores sobre el rendimiento de sus ofertas.

**Criterios de Aceptación:**
- Mostrar estado de publicación por portal (publicado, pendiente, error)
- Implementar actualizaciones en tiempo real mediante WebSockets
- Mostrar estadísticas de visualizaciones y candidaturas por oferta
- Crear gráficos y métricas de rendimiento
- Implementar notificaciones de cambios de estado
- Permitir pausar/reanudar publicaciones desde el dashboard
- Crear filtros y búsqueda de ofertas

**Prioridad:** Baja - Funcionalidad de monitoreo para versiones posteriores

**Estimación:** 13 puntos

**Asignado a:** Equipo de Frontend + Equipo de Backend

**Etiquetas:** Frontend, Backend, Dashboard, WebSockets, Analytics

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Ticket 1.8: Sistema de Plantillas de Ofertas

**Título:** Sistema de Plantillas de Ofertas

**Descripción:** Implementar un sistema que permita guardar y reutilizar plantillas de ofertas de empleo para agilizar el proceso de creación. Esta tarea es necesaria para mejorar la eficiencia de los reclutadores que crean ofertas similares frecuentemente.

**Criterios de Aceptación:**
- Permitir guardar ofertas como plantillas
- Implementar biblioteca de plantillas predefinidas por industria
- Permitir editar y eliminar plantillas personalizadas
- Implementar búsqueda y filtrado de plantillas
- Crear vista previa de plantillas antes de usar
- Permitir compartir plantillas entre usuarios del equipo
- Implementar versionado de plantillas

**Prioridad:** Baja - Funcionalidad de productividad para versiones posteriores

**Estimación:** 8 puntos

**Asignado a:** Equipo de Frontend + Equipo de Backend

**Etiquetas:** Frontend, Backend, Plantillas, Productividad

**Comentarios:**

**Enlaces:**

**Historial de Cambios:**

---

## Resumen de Estimaciones por Prioridad:

**Alta Prioridad (MVP):**
- Ticket 1.1: 8 puntos
- Ticket 1.2: 13 puntos  
- Ticket 1.3: 8 puntos
**Total MVP: 29 puntos**

**Media Prioridad (V2):**
- Ticket 1.4: 13 puntos
- Ticket 1.5: 21 puntos
- Ticket 1.6: 8 puntos
**Total V2: 42 puntos**

**Baja Prioridad (V3):**
- Ticket 1.7: 13 puntos
- Ticket 1.8: 8 puntos
**Total V3: 21 puntos**

**Total Historia de Usuario 1: 92 puntos**
