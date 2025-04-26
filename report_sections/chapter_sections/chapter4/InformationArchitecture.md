## 4.2. Information Architecture

Information Architecture es el proceso de estructurar, organizar y etiquetar el contenido de un sistema digital de forma lógica y usable, facilitando la navegación, el acceso eficiente a la información y la comprensión del producto por parte del usuario. En el contexto de ProP GMS, nuestra plataforma en la nube para la gestión de proyectos de ingeniería civil, la AI es fundamental para que los usuarios puedan acceder fácilmente a funciones críticas como la planificación de tareas, el control de presupuesto, la gestión documental y la elaboración del expediente técnico.

### 4.2.1. Organization Systems

En ProP GMS, la arquitectura de la información se diseña estratégicamente para ofrecer una experiencia de usuario clara, eficiente y adaptada a tres tipos principales de usuarios: contratistas, especialistas de área y contratantes. Cada grupo accede a diferentes módulos y niveles de interacción con el sistema, lo que exige una organización inteligente del contenido tanto en su estructura visual como en su categorización.

A nivel visual, el sistema aplica una **organización jerárquica** en módulos como el dashboard principal, donde se prioriza la presentación del estado general de los proyectos, hitos relevantes y alertas. Esta jerarquía visual ayuda especialmente a los contratantes, quienes necesitan una visión panorámica para la toma de decisiones. Por otro lado, se utiliza una **organización secuencial** en flujos como la creación de organizaciones, miembros y cronogramas, siguiendo pasos lógicos que guían a los contratistas o especialistas en el ingreso de datos complejos, minimizando errores. Además, en la gestión de cronogramas y seguimiento de hitos, se incorpora una **organización matricial**, útil para comparar variables interrelacionadas como tareas, fechas y responsables, especialmente valiosa para los especialistas de área.

Respecto a la **categorización de contenido**, se utiliza un **enfoque alfabético** en elementos como nombres de organizaciones, miembros y proyectos, lo cual agiliza la búsqueda en listas extensas. En los módulos de cronogramas y control de hitos, se aplica una **organización cronológica**, lo que permite a los usuarios revisar el progreso y evolución del proyecto en orden temporal. Asimismo, se estructura el **contenido por tópicos** en áreas como la documentación técnica o la configuración de entidades, agrupando funciones similares bajo secciones claras como "Organizaciones", "Miembros", "Proyectos" y "Cronogramas". Finalmente, la **organización por audiencia** permite ofrecer vistas y funcionalidades diferenciadas: los contratistas podrán gestionar proyectos y cronogramas, los especialistas editar hitos y controlar el avance, y los contratantes visualizar informes y estados generales.

Esta combinación de **estrategias organizativas** garantiza que cada usuario encuentre lo que necesita en el momento preciso, optimizando su productividad y reduciendo la fricción en el uso del sistema. ProP GMS no solo organiza proyectos, sino que también organiza la experiencia del usuario para que sea tan robusta como intuitiva.

### 4.2.2. Labeling Systems

En este sistema, se utilizan etiquetas claras y mínimas para guiar a los usuarios —principalmente **contratistas**— a través de la plataforma, asegurando que puedan encontrar y comprender fácilmente las funcionalidades disponibles. Las etiquetas han sido seleccionadas con simplicidad y coherencia en mente, promoviendo una navegación intuitiva y evitando la sobrecarga cognitiva.

Por ejemplo, la etiqueta **Subscription** está asociada con la selección y gestión de planes. Esta etiqueta permite a los **contratistas** identificar rápidamente dónde activar o cambiar su plan actual. La etiqueta **Payments** conduce a las secciones donde los usuarios pueden visualizar y completar transacciones relacionadas con su suscripción, y se encuentra estrechamente vinculada a **Invoices** y **Subscription**.

Por su parte, **Invoices** representa el historial de facturación y las notificaciones relacionadas con cargos pendientes o completados. Los usuarios la asocian con recordatorios y el resumen financiero de su actividad. La etiqueta **Authentication** engloba funcionalidades como **Login**, **Sign up**, recuperación de contraseña y seguridad de credenciales, agrupando todos los accesos de identidad bajo un mismo concepto comprensible.

La etiqueta **Profile** indica el espacio donde los usuarios pueden editar, actualizar o gestionar su información personal y profesional. **Notifications** alerta a los usuarios sobre eventos importantes, especialmente respecto a pagos, tareas asignadas o cambios en los proyectos. **Dashboard** funciona como el centro de control donde se muestra un resumen de **Projects**, fechas clave e indicadores de desempeño.

La etiqueta **Change Requests** se utiliza para representar las solicitudes de modificación al proyecto, ya sea por parte de la entidad contratante o el equipo técnico, y está vinculada al historial de cambios y sus estados de aprobación. **Tasks** contiene la información sobre tareas asignadas, fechas límite y seguimiento del progreso, mientras que **Meetings** corresponde a la sección dedicada a las reuniones del proyecto, con una asociación directa con **Tasks** y **Schedule**.

**Schedule** agrupa **Tasks**, **Milestones** y **Meetings** dentro de un formato visual de cronograma para facilitar la planificación y seguimiento del proyecto. La etiqueta **Projects** lleva a la lista de proyectos gestionados en la plataforma. Por su parte, **Members** indica el área donde se pueden gestionar los roles y participantes de cada proyecto, y **Organization** hace referencia a la estructura organizativa detrás del usuario, incluyendo configuración de suscripción y control de acceso de los miembros.

Como ejemplo concreto de representación de datos, un proyecto puede tener distintos estados a lo largo de su ciclo de vida. Las etiquetas como **Draft**, **In progress**, **On hold**, **Cancelled** y **Completed** permiten al usuario identificar rápidamente el estado actual del proyecto. Estas etiquetas son simples, consistentes y reflejan claramente el progreso del trabajo, lo que mejora la experiencia del usuario y reduce posibles ambigüedades.

Asimismo, la etiqueta **Contact** puede aparecer en el pie de página, pero se relaciona mentalmente con contenidos como **Support**, **Help Center** o redes sociales, ayudando al usuario a anticipar qué tipo de información encontrará, aunque esté distribuida en distintas secciones del sitio.

Este sistema asegura que todos los usuarios, sin importar su nivel técnico, puedan navegar la plataforma con confianza, gracias a etiquetas predecibles y significativas que reflejan sus necesidades y objetivos.

<div style="page-break-before: always;"></div>

### 4.2.3. SEO Tags and Meta Tags

Los SEO Tags y Meta Tags son elementos fundamentales del código HTML que contribuyen significativamente al posicionamiento de un sitio web en los motores de búsqueda (SEO). Además, permiten definir cómo se muestra la información de la página cuando se comparte en redes sociales o aparece en los resultados de búsqueda de Google. A continuación, se detallan los SEO Tags y Meta Tags correspondientes a cada nivel.

<div style="font-size: 22px;">
  <strong>Landing Page</strong>
</div>

La Landing Page es la página pública principal del sitio. Su objetivo es atraer tráfico orgánico, mejorar el posicionamiento en motores de búsqueda y generar conversiones (registro, contacto, etc.). Por ello, requiere etiquetas orientadas al SEO, visibilidad y marketing digital.

**Title**

Propósito: Define el título que aparece en la pestaña del navegador y en los resultados de búsqueda.
```html
<title>Civil Engineering Project Management in the Cloud with ProP GMS</title>
```

**Meta Description**

Propósito: Resumen del contenido de la página. Aparece debajo del título en Google y afecta directamente la tasa de clics (CTR).
```html
<meta name="description" content="Optimize your civil engineering projects with our cloud-based platform. Planning, budgeting, technical files, and document management all in one place.">
```

**Meta Keywords**

Propósito: Palabras clave relacionadas con el contenido. Aunque tienen poco impacto en SEO moderno, aún se usan en algunas plataformas
```html
<meta name="keywords" content="civil engineering, project management, construction planning, budgeting, document control, cloud engineering software, technical files">
```

**Author**

Propósito: Especifica al autor del sitio o equipo de desarrollo.
```html
<meta name="author" content="Galaxia Wonder">
```

**Copyright**

Propósito: Se utiliza para informar que el conteniedo del sitio web está protegido por derechos de autor.
```html
<meta name="copyright" content="© 2025 Galaxia Wonder. All rights reserved.">
```

**Character encoding**

Propósito: Especificar la codificación de caracteres que debe utilizar el navegador al interpretar el contenido de una página HTML.
```html
<meta charset="utf-8">
```

<div style="page-break-before: always;"></div>

<div style="font-size: 22px;">
  <strong>Web Application</strong>
</div>

La Web Application es el panel privado para usuarios registrados. Aquí el enfoque no es atraer visitantes, sino mejorar la experiencia de usuario y mantener orden y estructura en la interfaz.

**Title**

Propósito: Muestra el nombre del proyecto activo o sección dentro del dashboard.
```html
<title>ProP GMS - Project Control</title>
```

**Meta Description**

Propósito: Aunque esta parte no se indexa, tener una descripción mejora la organización del contenido en navegadores o apps conectadas.
```html
<meta name="description" content="Monitor your projects, manage tasks, control budgets, and upload technical documentation from a single dashboard.">
```

**No Index**

Propósito: Evita que los motores de búsqueda indexen el dashboard privado.
```html
<meta name="robots" content="noindex, nofollow">
```

**Author**

Propósito: Especifica al autor del sitio o equipo de desarrollo.
```html
<meta name="author" content="Galaxia Wonder">
```

**Copyright**

Propósito: Se utiliza para informar que el conteniedo del sitio web está protegido por derechos de autor.
```html
<meta name="copyright" content="© 2025 Galaxia Wonder. All rights reserved.">
```

<div style="page-break-before: always;"></div>

### 4.2.4. Searching Systems

El sistema de búsqueda de **ProP GMS** ha sido diseñado para brindar a los usuarios una experiencia fluida, intuitiva y rápida a la hora de encontrar información específica dentro de un entorno con múltiples entidades y un alto volumen de datos. Las búsquedas están orientadas a tres perfiles principales de usuario: **contratistas**, **especialistas** y **entidades contratantes**, quienes interactúan con **Projects**, **Schedules**, **Teams**, **Tasks**, **Documents** y **Organizations**.

Desde la perspectiva del usuario, la funcionalidad de búsqueda busca minimizar la frustración y maximizar la eficiencia, permitiendo encontrar lo que se necesita en pocos pasos y con gran precisión.

El sistema permitirá búsquedas por texto directo. Esto significa que los usuarios podrán ingresar términos como el nombre de un **Project**, un **Organization Member** o una **Specialty**, y el sistema ofrecerá coincidencias relevantes. Por ejemplo, al escribir **Topography**, se podrán mostrar **Tasks**, **Meetings** o **Organization Members** que tengan esa especialidad.

También será posible buscar por **email** o **username**. Esta funcionalidad está especialmente pensada para facilitar la gestión de miembros en **Organizations** o **Projects**, reduciendo el tiempo que normalmente se emplea en la búsqueda manual dentro de listas extensas.

La búsqueda estará segmentada por tipo de entidad, lo cual quiere decir que el usuario podrá limitar los resultados según el contenido que necesite explorar: **Projects**, **Tasks**, **Meetings**, **Milestones**, **Organization Members**, entre otros.

Adicionalmente, el sistema contará con filtros por estado de entidad. Uno de los más importantes será el estado del proyecto (**ProjectStatus**), que ayuda al usuario a enfocar su búsqueda en proyectos que se encuentran en fases como **BASIC_STUDIES**, **DESIGN_IN_PROGRESS**, **UNDER_REVIEW**, **CHANGE_REQUESTED**, **CHANGE_PENDING** o **APPROVED**.

Otro filtro esencial será el estado de las tareas (**TaskStatus**), que permitirá a los **especialistas** y **coordinadores** ver rápidamente qué **Tasks** están en estado **DRAFT**, **PENDING**, **SUBMITTED**, **APPROVED** o **REJECTED**.

El filtro de especialidad técnica (**Specialty**) permitirá segmentar la información según disciplinas profesionales como **ARCHITECTURE**, **STRUCTURES**, **HSA**, **TOPOGRAPHY**, **SANITATION**, **ELECTRICITY** o **COMMUNICATIONS**. Esto es especialmente útil cuando se desea encontrar **Tasks** o **Organization Members** con un perfil técnico específico.

El objetivo principal del sistema de búsqueda de **ProP GMS** es que **contratistas**, **especialistas** y **entidades contratantes** accedan sin fricciones a la información crítica que necesitan, en un entorno ordenado, filtrable y accesible desde cualquier módulo del producto.

### 4.2.5. Navigation Systems

El sistema de navegación de **ProP GMS** está diseñado para guiar a los usuarios de forma intuitiva y eficiente a través de todos los componentes del producto, ya sea desde la **Landing Page** o dentro de la **Web Application**. Se ha estructurado una experiencia coherente que facilite la orientación y permita a los usuarios alcanzar sus objetivos sin fricciones.

En la **Landing Page**, se implementa una navegación clara mediante un **Header** fijo que contiene enlaces ancla hacia secciones clave como **About Us**, **Overviews**, **About the Product**, **Testimonials** y **Contact Us**, junto con una selección de idioma. El **Footer** también ofrece accesos rápidos a secciones auxiliares.

Dentro de la **Web Application**, **ProP GMS** ha sido diseñada con una estructura adaptable a los distintos perfiles de usuario: **contratistas**, **especialistas** y **entidades contratantes**. La interfaz utiliza una **Sidebar** fija que agrupa las funcionalidades principales por categoría. También se emplean **breadcrumbs** y cabeceras contextuales.

Para los **contratistas**, la navegación se centra en el control y la gestión integral de los **Projects**. Desde el módulo **Dashboard**, pueden acceder rápidamente a **Projects**, crear nuevos, asignar **Organization Members**, establecer objetivos y subir **Documents**. La navegación continúa hacia **Schedules**, **Tasks** y **Meetings**, que están interconectados dentro de cada **Project**. También tienen acceso a la gestión de **Organizations** y **Organization Members**.

Los **especialistas** comparten un flujo similar al de los **contratistas**, pero con funcionalidades ajustadas a su nivel de permisos. Desde su **Dashboard**, acceden a los **Projects** en los que participan, gestionan sus **Tasks**, asisten a **Meetings**, colaboran en el **Schedule** y actualizan su **Profile**.

Las **entidades contratantes** acceden a una navegación centrada en el monitoreo del **Project**. Desde su panel inicial, ingresan a la vista de **Projects**, consultan el avance general mediante los **Schedules**, y revisan la sección de **Change Requests** para enviar comentarios o requerimientos relacionados con entregables y fechas.

Todo el sistema ha sido diseñado para ofrecer claridad y control a los **contratistas**, facilitando una comunicación efectiva y una toma de decisiones informada por parte de las **entidades contratantes**.