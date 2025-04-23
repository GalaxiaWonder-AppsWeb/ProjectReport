## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

En Galaxia Wonder hemos adoptado una serie de herramientas tanto familiares como más recientes para el diseño, desarrollo y despliegue de nuestra solución de software. En la siguiente tabla a continuación, se presentan las principales herramientas a utilizar por el equipo.

<table>
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Propósito de uso en el proyecto</th>
            <th>Enlace de referencia / descarga</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>UXPressia</td>
            <td><strong>UX/UI Design:</strong> Artefactos de UX</td>
            <td><a href="https://uxpressia.com/" target="_blank">UXPressia Web Application</a></td>
        </tr>
        <tr>
            <td>Miro</td>
            <td><strong>UX/UI Design:</strong> As-Is & To-Be Scenario Mapping</td>
            <td><a href="https://miro.com/es/app/" target="_blank">Descargar Miro</a></td>
        </tr>
        <tr>
            <td>Figma</td>
            <td><strong>UX/UI Design:</strong> Wireframes, Mockups & Prototyping</td>
            <td><a href="https://www.figma.com/es-la/downloads/" target="_blank">Descargar Figma</a></td>
        </tr>
        <tr>
            <td>LucidChart</td>
            <td><strong>UX/UI Design:</strong> Wireflows & Userflows</td>
            <td><a href="https://www.lucidchart.com/" target="_blank">LucidChart Web</a></td>
        </tr>
        <tr>
            <td>Vertabelo</td>
            <td><strong>Software Architecture Design:</strong> Database Diagram</td>
            <td><a href="https://vertabelo.com/" target="_blank">Vertabelo Web</a></td>
        </tr>
        <tr>
            <td>PlantUML</td>
            <td><strong>Software Architecture Design:</strong> UML y C4 Model</td>
            <td><a href="https://plantuml.com/es/" target="_blank">PlantUML Web</a></td>
        </tr>
        <tr>
            <td>VSCode</td>
            <td><strong>IDE:</strong> Editor de código ligero y versátil para múltiples lenguajes</td>
            <td><a href="https://code.visualstudio.com/" target="_blank">Descargar VSCode</a></td>
        </tr>
        <tr>
            <td>WebStorm</td>
            <td><strong>IDE:</strong> Desarrollo especializado en JavaScript y frameworks modernos</td>
            <td><a href="https://www.jetbrains.com/webstorm/" target="_blank">WebStorm Web</a></td>
        </tr>
        <tr>
            <td>Rider</td>
            <td><strong>IDE:</strong> Desarrollo en C# y .NET multiplataforma</td>
            <td><a href="https://www.jetbrains.com/rider/" target="_blank">Rider Web</a></td>
        </tr>
        <tr>
            <td>C#</td>
            <td><strong>Lenguaje de Programación:</strong> Backend moderno con tipado fuerte</td>
            <td><a href="https://learn.microsoft.com/en-us/dotnet/csharp/" target="_blank">Documentación de C#</a></td>
        </tr>
        <tr>
            <td>Node.js</td>
            <td><strong>Entorno de Ejecución:</strong> JavaScript del lado del servidor</td>
            <td><a href="https://nodejs.org/" target="_blank">Descargar Node.js</a></td>
        </tr>
        <tr>
            <td>npm</td>
            <td><strong>Gestor de Paquetes:</strong> Manejo de dependencias para proyectos JS</td>
            <td><a href="https://www.npmjs.com/" target="_blank">Sitio de npm</a></td>
        </tr>
        <tr>
            <td>Vue.js</td>
            <td><strong>Framework:</strong> Desarrollo de aplicaciones web SPA con JavaScript</td>
            <td><a href="https://vuejs.org/" target="_blank">Vue.js Web</a></td>
        </tr>
        <tr>
            <td>.NET</td>
            <td><strong>Framework:</strong> Plataforma para aplicaciones backend y frontend modernas</td>
            <td><a href="https://dotnet.microsoft.com/" target="_blank">Sitio oficial .NET</a></td>
        </tr>
    </tbody>
</table>

### 5.1.2. Source Code Management

En Galaxia Wonder, la gestión del código fuente se realiza mediante Git como sistema de control de versiones, y GitHub como plataforma de alojamiento colaborativo y descentralizado. Esta estructura facilita la colaboración entre equipos distribuidos y permite un control riguroso del ciclo de vida del software.

El proyecto está organizado en varios repositorios, según la arquitectura modular de las soluciones tecnológicas utilizadas:

- Landing Page (Vue.js + Tailwind CSS):  
  [https://github.com/GalaxiaWonder-AppsWeb/LandingPage](https://github.com/GalaxiaWonder-AppsWeb/LandingPage)

- FrontEnd Web Application (Vue.js SPA con Vite):  
  [https://github.com/GalaxiaWonder-AppsWeb/FrontEnd](https://github.com/GalaxiaWonder-AppsWeb/FrontEnd)

- RESTful API (C# + ASP.NET Core):  
  [https://github.com/GalaxiaWonder-AppsWeb/API](https://github.com/GalaxiaWonder-AppsWeb/API)

- ProP GMS Web Service (Arquitectura modular basada en .NET):  
  [https://github.com/GalaxiaWonder-AppsWeb/Platform](https://github.com/GalaxiaWonder-AppsWeb/Platform)

Para su gestión interna, se aplicará GitFlow. Se explican a continuación las ramas a crear, así como las convenciones a utilizar para nombrarlas:

**RAMAS PRINCIPALES**

- **main**: Rama principal de producción. Aquí se encuentran las versiones estables del proyecto, listas para ser desplegadas. Toda publicación oficial se hace desde esta rama.

- **develop**: Rama de desarrollo. Aquí se integran las nuevas funcionalidades antes de ser lanzadas a producción. Es la base para las ramas de tipo *feature*, *release* y *bugfix*.

**RAMAS SECUNDARIAS**

- **feature/**: Ramas para el desarrollo de nuevas funcionalidades. Se crean a partir de `develop` y, una vez completadas, se integran de nuevo en `develop`.  
  - **Convención de nombres**:  
    `feature/story-id`  
    Ejemplo: `feature/us77`

- **bugfix/**: Ramas para la correción de errores detectados en fase de desarrollo. Se crean a partir de `develop` y, una vez completadas, se integran de nuevo en `develop`.  
  - **Convención de nombres**:  
    `bugfix/story-id`  
    Ejemplo: `bugfix/us82`

- **release/**: Ramas para preparar una nueva versión de producción. Se crean desde `develop` cuando ya se ha alcanzado un conjunto estable de funcionalidades. Sirven para realizar pruebas, ajustes menores y documentación. Al finalizar, se integran en `main` y `develop`.  
  - **Convención de nombres**:  
    `release/x.y.z`  
    Ejemplo: `release/1.0.0`

- **hotfix/**: Ramas para corregir errores críticos detectados tardíamente en producción. Se crean desde `main` y se integran tanto en `main` como en `develop` (o en `release`, si hubiere alguna rama de ese tipo activa).  
  - **Convención de nombres**:  
    `hotfix/story-id`  
    Ejemplo: `hotfix/swr35`
