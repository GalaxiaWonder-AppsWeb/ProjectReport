## 2.4. Ubiquitous Language

### 2.4.1. Core

**Project Management (Gestión de proyectos)**

El bounded context de Project Management está dedicado a la planificación, ejecución y seguimiento de proyectos de construcción o ingeniería. Su enfoque se centra en la coordinación de tareas, el manejo de recursos, el monitoreo del progreso y la organización de roles. Este contexto asegura que todos los aspectos del proyecto estén alineados con los objetivos, plazos y presupuestos definidos, y que los especialistas trabajen de forma eficaz hacia los entregables acordados.

**1. Project (Proyecto):** Unidad estructurada de trabajo con objetivos, fechas y alcance definidos. Incluye múltiples tareas, hitos y recursos humanos, y está asociada a un contrato específico y tiene como producto final desarrollo de un expediente técnico. <br>
**2. Technical File (Expediente técnico):** El expediente técnico es un conjunto ordenado y sistemático de documentos que sustentan la viabilidad técnica, económica, ambiental y legal de un proyecto. Incluye planos, especificaciones, presupuestos, cronogramas, estudios de impacto, y otros documentos necesarios para su aprobación y ejecución.<br>
**3. Contractor (Contratista / Proyectista):** Persona responsable de ejecutar el proyecto. Firma un contrato con la entidad contratante y administra los recursos y personal de campo.<br>
**4. Coordinator (Coordinador):** Rol dentro del sistema encargado de la gestión operativa y documental del proyecto.<br>
**5. Specialist (Especialista):** Profesional técnico que participa en el proyecto con funciones específicas: ingeniero estructural, sanitario, eléctrico, arquitecto, etc.<br>
**6. Contracting entity (Entidad contratante):** Persona que encarga y financia el proyecto. Define los lineamientos y da seguimiento a la planificación del proyecto.<br>
**7. Schedule (Cronograma):** Representación temporal del proyecto. Incluye la calendarización de cada hito, tarea, actividades como reuniones y su duración estimada.<br>
**8. Milestone (Hito):** Evento clave dentro del cronograma que marca un avance importante o entregable específico del proyecto.<br>
**9. Task (Tarea):** Actividad puntual y necesaria asignada al especialista de área para alcanzar uno o más hitos del proyecto.<br>
**10. Meeting (Reunión):** Espacio programado para coordinar, resolver problemas o validar avances del proyecto.<br>
**11. Memorandum (Ayuda Memoria):** Documento breve que resume una reunión, visita o decisión técnica.<br>
**12. Risk Assessment Sheet (Ficha de riesgo):** Documento que identifica y evalúa riesgos potenciales del proyecto.<br>
**13. Descriptive memories of specialty (Memorias descriptivas de especialidad):** Descripciones técnicas de cada disciplina (estructura, sanitarios, eléctricos, etc.) que justifican diseño y soluciones propuestas.<br>
**14. Technical specifications (Especificaciones técnicas):** Detalles de calidad, materiales y ejecución para cada elemento del proyecto.<br>
**15. Budget (Presupuesto):** Estimación total de costos del proyecto, desglosado por partidas y rubros.<br>
**16. Quantity Take-Off (Metrados):** Cálculo de cantidades de obra (volúmenes, áreas, longitudes) basado en planos.<br>
**17. Medium Voltage System (Sistema de media tensión):** Infraestructura eléctrica que opera entre 1 kV y 35 kV. Se usa para distribución de energía en obras que requieren alto consumo (edificios, plantas, etc.).<br>
**18. Soil Mechanics Study (Estudio de mecánica de suelos):** Análisis de las propiedades del terreno donde se construirá, clave para diseño de cimentaciones.<br>
**19. Topographic Survey (Levantamiento topográfico):** Registro de la forma, elevación y características del terreno. Sirve de base para el diseño de planos.<br>
**20. Plains (Planos):** Representaciones gráficas del proyecto (arquitectura, estructuras, instalaciones, etc.). Estos pueden ser planos de estado actual o planos de especialidad.<br>
**21. Technical File Preparation Budget (Presupuesto de elaboración del expediente técnico):** Estimación del costo asociado al desarrollo completo del expediente técnico del proyecto.<br>
**22. Performance (Desempeño):** Indicador de cumplimiento de los hitos en el plazo previsto.<br>


**Change Management (Gestión del cambio)**

Este contexto se encarga de gestionar y documentar todas las modificaciones que afectan el proyecto durante su ejecución, ya sea en alcance, plazos, costos o diseño. Incluye el manejo de cambios contractuales formales, consultas técnicas, discrepancias entre planos y rediseños en campo. La trazabilidad y aprobación adecuada de estos cambios es crítica para mantener el control y la transparencia del proyecto.

**1. Change (Cambio):** Un término general que se refiere a cualquier modificación realizada al alcance, costo, cronograma o especificaciones técnicas del proyecto original.<br>
**2. Change Order (Adicional de obra):** Documento formal que aprueba costos o trabajos adicionales fuera del contrato original. Puede originarse por solicitud del cliente, incompatibilidades técnicas o condiciones imprevistas en obra.<br>
**3. Change Request (Solicitud de cambio):** Condición o especificación técnica o requisito solicitada por la Entidad Contratante (o su representante) durante el proceso de elaboración de un expediente técnico.<br>
**4. Technical query (Consulta técnica):** Pregunta formal que se genera durante la obra cuando hay ambigüedad o duda en la documentación técnica (planos, metrados, especificaciones).<br>
**5. Incompatibility of plans (Incompatibilidad de planos):** Discrepancia entre planos de distintas especialidades o versiones, que impide o dificulta la ejecución directa de la obra. Debe resolverse mediante coordinación técnica y puede derivar en una consulta técnica o un cambio de diseño.<br>
**6. Field redesign (Replanteo de obra):** Rediseño parcial que se realiza en campo debido a condiciones imprevistas, errores en planos o cambios validados.<br>
**7. Contractor (Contratista / Proyectista):** Persona ejecutora del proyecto. Responsable de la supervisión del diseño conforme a los planos, especificaciones y contrato.<br>
**8. Contracting entity (Entidad contratante):** Persona que encarga y financia el proyecto. Define los lineamientos y da seguimiento a la planificación del proyecto.<br>
**9. Contracting entity supervisor (Supervisor):** Profesional que representa a la entidad contratante en obra. Se encarga de supervisar la ejecución, verificar metrados, validar planos, y evaluar cualquier consulta o cambio.<br>
**10. Site Worker (Operario de obra):** Persona que ejecuta la obra, es decir, instala, construye, excava, vacía o pinta, dependiendo de su especialidad.<br>
<div style="page-break-before: always;"></div>

### 2.4.2. Support

**Organizations (Organizaciones)**

El contexto de organizaciones se encarga de la estructura interna de una empresa consultora de obra. Aquí se administran las organizaciones, sus miembros e invitaciones.

**1. Organization (Organización):** Representa a la empresa consultora de obra dentro del sistema.<br>
**2. Legal name (Razón ocial):** Nombre legal bajo el cual la empresa está registrada y opera, y es utilizado en todos los trámites y documentos legales.<br>
**3. Commercial name (Nombre comercial):** Nombre con el que se identifica su actividad económica, diferenciándose de otras empresas, ya sean similares o diferentes.<br>
**4. RUC (RUC):** Se trata de un identificador que identifica a una empresa como contribuyente para cualquier tipo de trámite o declaración que el contribuyente desee realizar en la Sunat.<br>
**5. Organization member (Miembro de organización):** Se trata de un trabajador de la organización. Es un empleado que se ha vinculado a la empresa consultora y que puede ser ingresado como miembro de un proyecto.<br>
**6. Worker (Trabajador):** Se trata del rol de los trabajadores dentro de la organización.<br>


**Notifications (Notificaciones)**

El contexto de notificaciones se encarga de gestionar el envío de mensajes relevantes dentro del sistema. Estos mensajes son generados por un coordinador y enviados a los usuarios correspondientes, quienes deben tomar conocimiento o realizar alguna acción sobre eventos o situaciones específicas. Las notificaciones se priorizan según su urgencia y se entregan a través de canales definidos.

**1. Notification (Notificación):** Representa un mensaje generado por un coordinador. La notificación comunica información importante a uno o más destinatarios para que tomen conocimiento o acción sobre una situación específica.<br>
**2. Sender (Remitente):** Es la entidad que origina la notificación. Puede ser un usuario o el propio sistema de manera automática.<br>
**3. Addressee (Destinatario):** Es el usuario designado para recibir la notificación.<br>
**4. Notification priority (Prioridad de notificación):** Indica el nivel de urgencia o criticidad de la notificación.<br>
**5. Coordinator (Coordinador):** Rol asignado a un usuario que puede ser miembro de la organización o ser parte de la entidad contratante. Envía notificación de reuniones a los especialistas, notificaciones de entrega de tareas.<br>
**6. Specialist (Especialista):** Rol asignado a un miembro de la organización o subcontratado. Reciben notificaciones de reuniones o notificaciones de tareas.<br>


**Files Management (Gestión de archivos)**

Este contexto gestiona los archivos dentro del sistema. Modela los archivos en carpetas y los relaciona a la sección donde se encuentran en el proyecto.

**1. Folder (Carpeta):** Es un espacio que agrupa archivos del expediente técnico. Puede encontrarse dentro de otra carpeta y puede tener carpetas dentro.<br>
**2. File (Archivo):** Es un elemento de una carpeta. Guarda información valiosa del expediente técnico en formato pdf, word, etc.<br>
**3. Workspace (Espacio de trabajo):** Es el espacio de trabajo que adquiere una organización para poder planificar sus proyectos dentro del sistema.<br>

### 2.4.3. Generic

**Identity and Access Management (Gestión de identidad y acceso)**

El contexto de Identity and Access Management (IAM) se encarga de la asignación de roles y permisos A través de este contexto se asegura la correcta administración de accesos y roles, permitiendo una gestión eficiente y segura de los proyectos y equipos.

**1. Organization (Organización):** Unidad estructural dentro del sistema que representa a una empresa consultora. Agrupa usuarios (miembros) bajo una misma identidad corporativa y permite la gestión centralizada de proyectos, equipos y recursos humanos asociados.<br>
**2. Profile (Perfil):** Representación profesional de un usuario. Contiene su información personal relevante de acuerdo a su tipo de usuario.<br>
**3. User Type (Tipo de usuario):** Establece el tipo de usuario. Este puede ser Miembro de Organización o Entidad Contratante.<br>
**4. Organization Member (Miembro de Organización):** Tipo de usuario que pertenece a una Organización y trabaja en la elaboración de expedientes técnicos en un proyecto de esta.<br>
**5. ID Number (Número de documento):** Identificador legal de la entidad contratante o empresa consultora. En el caso de Entidades Contratantes, este puede ser DNI o RUC, según se trata de una persona natural o jurídica. En el caso de Empresas Consultoras, se tratará siempre de un RUC.<br>
**6. Contact Information (Información de contacto):** Grupo de datos como correo, número de teléfono y/o redes sociales de un usuario que permiten establecer contacto con este de forma externa a la plataforma.<br>
**7. License Number (Código de colegiado):** Documento o registro oficial que respalda la capacitación o habilitación del usuario para ejercer determinada función técnica.<br>
**8. Contractor (Contratista / Proyectista):** Rol asignado a un único miembro de la organización, típicamente el gerente. Se encarga de añadir miembros a su organización, gestionar todos los proyectos de la organización en general.<br>
**9. Contracting entity (Entidad contratante):** Rol asignado a un usuario ajeno a la organización. Puede solicitar cambios y realizar seguimiento a un proyecto por el que haya contratado al proyectista.<br>
**10. Project manager (Jefe de proyecto):** Rol asignado a un miembro de la organización. Este rol se encarga de supervisar el desarrollo de un proyecto, organizar reuniones de coordinación y garantizar el cumplimiento de las expectativas del cliente y las normas vigentes.<br>
**11. Coordinator (Coordinador):** Rol asignado a un usuario que puede ser miembro de la organización o ser parte de la entidad contratante. Apoya al jefe de proyecto en cuestiones más específicas, desempeñando las mismas o similares funciones de manera constante.<br>
**12. Specialist (Especialista):** Rol asignado a un miembro de la organización o subcontratado. Se encarga de realizar y entregar tareas para cumplir hitos relacionados a su especialidad.<br>
**13. Speciality (Especialidad):** Área técnica en la que el usuario se desempeña profesionalmente, como arquitectura, estructuras, saneamiento, electricidad, etc.<br>
**14. Architect (Arquitecto):** Subrol de especialista encargado del diseño arquitectónico del proyecto. Se responsabiliza de la organización espacial, funcional y estética del edificio, elaborando planos arquitectónicos y coordinando con las demás especialidades.<br>
**15. Health and security consultant (Consultor en salud y seguridad):** Subrol de especialista responsable de identificar y prevenir riesgos laborales y de obra. Asesora al equipo de diseño en materia de seguridad desde la etapa de anteproyecto y elabora planes de seguridad y salud aplicables a la ejecución.<br>
**16. Surveyor (Topógrafo):** Subrol encargado de realizar levantamientos del terreno para generar información precisa sobre cotas, pendientes y límites del predio. Esta información sirve como base para el diseño y la ejecución del proyecto.<br>
**17. Structural Engineer (Ingeniero estructural):** Subrol de especialista que diseña y calcula la estructura portante del proyecto. Se encarga de definir elementos como vigas, columnas y fundaciones, asegurando estabilidad y seguridad frente a cargas permanentes y eventuales.<br>
**18. Sanitary Engineer (Ingeniero sanitario):** Subrol de especialista responsable del diseño de sistemas de agua potable, desagüe, drenaje pluvial y ventilación sanitaria. Garantiza el funcionamiento eficiente y seguro de las instalaciones sanitarias del proyecto.<br>
**19. Electrical Engineer (Ingeniero eléctrico):** Subrol de especialista encargado de diseñar las instalaciones eléctricas del proyecto, incluyendo iluminación, tomacorrientes, tableros y protección. Asegura el cumplimiento de normas técnicas y la eficiencia energética.<br>
**20. Communications engineer (Ingeniero de comunicaciones):** Subrol de especialista que diseña los sistemas de telecomunicaciones del edificio, como red de datos, telefonía, CCTV y control de acceso. Coordina con el equipo eléctrico y arquitectónico para la correcta integración de estas redes.<br>


**Billing (Facturación)**

Contexto encargado de gestionar la generación, emisión y control de facturas relacionadas a los contratos del proyecto. Administra montos, conceptos, fechas, estados de pago y documentos relacionados con cobros por servicios o entregables.

**1. Invoice (Factura):** Documento comercial que detalla los servicios prestados o entregables completados, junto con sus respectivos montos, impuestos y fechas. Es generado por el contratista y dirigido a la entidad contratante.<br>
**2. Billing Item (Ítem de facturación):** Elemento individual dentro de una factura que representa un concepto específico facturado (por ejemplo, avance de obra, expediente entregado, adicional aprobado).<br>
**3. Payment Status (Estado de pago):** Indica la situación actual de una factura: pendiente, en revisión, aprobada, rechazada o pagada.<br>
**4. Pending (Pendiente):** La factura ha sido emitida, pero aún no ha sido revisada por la entidad contratante. Está a la espera de validación.<br>
**5. Under Review (En revisión):** La factura está siendo evaluada por el supervisor o responsable de control. Se verifica su consistencia con el contrato, los entregables y los documentos adjuntos.<br>
**6. Approved (Aprobada):** La factura ha sido validada por la entidad contratante. Se encuentra autorizada para su pago dentro del plazo establecido.<br>
**7. Rejected (Rechazada):** La factura fue evaluada y no cumple con los requisitos contractuales o presenta errores. Se debe corregir y reenviar.<br>
**8. Paid (Pagada):** La factura ha sido cancelada total o parcialmente por la entidad contratante. El pago ha sido realizado al contratista.<br>


**Subscription (Suscripción)**

Bounded context encargado de gestionar el ciclo de vida de las suscripciones de usuarios o entidades dentro del sistema. Incluye la administración de planes, fechas de inicio y vencimiento, renovaciones, periodos de prueba, tarifas y estados. Este contexto asegura el control sobre el acceso a funcionalidades o servicios sujetos a suscripción, permitiendo aplicar reglas comerciales, restricciones y notificaciones automatizadas según el estado de cada suscripción.

**1. Subscription (Suscripción):** Acuerdo que permite a un usuario o entidad acceder a servicios, funcionalidades o información durante un periodo definido, bajo condiciones específicas (como tarifas, límites de uso, etc.).<br>
**2. Subscription Plan (Plan de suscripción):** Conjunto de condiciones que definen el nivel de acceso, duración, precio y beneficios de la suscripción. Puede haber distintos planes según el perfil del usuario.<br>
**3. Start Date (Fecha de inicio):** Fecha en la que comienza la vigencia de la suscripción. Marca el momento desde el cual el usuario puede hacer uso del servicio contratado.<br>
**4. End Date (Fecha de finalización):** Fecha en la que termina la vigencia de la suscripción, salvo que sea renovada o extendida.<br>
**5. Renewal (Renovación):** Acción de extender la suscripción una vez vencido el periodo anterior, ya sea de forma automática o manual.<br>
**6. Subscription Fee (Tarifa de suscripción):** Monto que el usuario debe pagar para acceder al servicio dentro del plan elegido.<br>

**Payments (Pagos)**

Bounded context encargado de gestionar el procesamiento de pagos dentro del sistema. Incluye la ejecución de transacciones mediante pasarelas externas, la validación de métodos de pago, la autorización y confirmación de operaciones, así como el seguimiento de estados de cada transacción

**1. Payment (Pago):** Representa la acción de pagar una factura u obligación<br>
**2. Payment Method (Método de pago):** Representa el método de pago como tarjeta de crédito, débito, transferencia bancaria.<br>
**3. Transaction (Transacción):** Representa el intento de pago y sus datos (monto, método, resultado, etc.).<br>
**4. Payment reference (Referencia de pago):** Código único para asociar pago con factura.<br>