---
title: Arquitectura de Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: Project Server 2013 integra funciones de administración de proyectos a lo largo de una granja de servidores de SharePoint y permite el uso de Project Online con un modelo de objetos de cliente (CSOM) y una interfaz de OData para los datos de informes.
ms.openlocfilehash: 633532d85b4d910c11a284231cb9a4c3e5a549cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394100"
---
# <a name="project-server-architecture"></a>Arquitectura de Project Server

Project Server 2013 integra funciones de administración de proyectos a lo largo de una granja de servidores de SharePoint y permite el uso de Project Online con un modelo de objetos de cliente (CSOM) y una interfaz de OData para los datos de informes.
   
Project Server 2013 es un sistema de varios niveles que extiende la arquitectura introducida en Office Project Server 2007. Cambios en la arquitectura incluyen la asociación del servicio de aplicación del proyecto con las colecciones de sitios de SharePoint, la adición de algunos objetos de negocios en el web front-end (WFE), el modelo de objetos de cliente (CSOM) para el acceso remoto, una sola base de datos de Project, un Interfaz de OData para las tablas de informes y vistas, integración de Windows Workflow Foundation versión 4 (WF4) a través de 1.0 de cliente de administrador de flujo de trabajo en la nube o en un servidor local y receptores de eventos remotos que pueden tener acceso a varios servidores de Project instalaciones. Además de las soluciones personalizadas de locales, puede crear aplicaciones que incluyen receptores de eventos remotos y los componentes que tienen acceso a las interfaces CSOM y OData.
  
El nivel front-end incluye aplicaciones de terceros, Project Web App y Project Professional 2013. Aplicaciones cliente se comunican con el nivel intermedio a través de Project Server Interface (PSI) o a través de los extremos CSOM, que a su vez se comunican con la capa de objetos de negocio y de la PSI. Acceso de base de datos está integrado en los objetos de negocios. El sistema de eventos de Project Server puede tener acceso a los controladores de eventos locales y receptores de eventos remotos. El servicio de cálculo de Project implementa el motor de programación de Project Professional en Project Server. Las aplicaciones cliente no (o no se debe) tener acceso directamente a la base de datos del proyecto; Project Server oculta los objetos de negocios de los clientes.
  
> [!NOTE]
> Project Server se basa en la arquitectura de SharePoint. Para obtener información sobre la arquitectura de SharePoint Server 2013 y el modelo de aplicaciones de SharePoint, vea la sección de *Introducción al desarrollo de SharePoint* en la documentación para desarrolladores de Office 2013. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Integración con las recopilaciones de sitios de SharePoint

El servicio de aplicación de proyecto en Project Server 2013 se puede asociar con una colección de sitios de SharePoint para su uso con listas de tareas de SharePoint, el servicio de aplicación de proyecto también puede importar una lista de tareas de SharePoint como un proyecto de empresa para todo el servidor de Project control. Con una lista de tareas de SharePoint, SharePoint Team Services mantiene el sitio del proyecto en una colección de sitios; Project Professional puede sincronizarse con y actualizar la lista de tareas. Un sitio de proyecto puede ser una lista de tareas de SharePoint independiente o una lista de tareas que se sincroniza con un archivo .mpp; el archivo .mpp puede almacenarse localmente o en una biblioteca de SharePoint. 
  
Project Server mantiene los proyectos cuando tiene control total; Project Professional guarda datos directamente en Project Server. La tabla 1 se compara el comportamiento de una lista de tareas, el elemento web de programación y otras funciones para el control de las listas de tareas de SharePoint y para los proyectos importados cuando Project Server tiene control total. El elemento web de programación contiene la cuadrícula en la página de Project Web App, donde puede editar una programación de proyecto. El modo vinculado es donde se escriben una vez los datos de estado para las tareas y partes de horas; en el modo de entrada único, los datos de estado de tarea se especifican por separado de los partes de horas.
  
**Tabla 1. Comparación de una lista de tareas de SharePoint y el control total**

| Característica | Lista de tareas | Control total |
|:-----|:-----|:-----|
|**Lista de tareas en SharePoint** <br/> |Lectura/escritura  <br/> |Solo lectura  <br/> |
|**Elemento web de programación** <br/> |Solo lectura  <br/> |Lectura/escritura  <br/> |
|**Informes** <br/> |Informes avanzados con Project Server  <br/> |Informes avanzados con Project Server  <br/> |
|**Otras funciones de Project Server** <br/> | Función bloqueada:  <br/>-Ediciones del proyecto server-side con Project Web App o aplicaciones de cliente personalizadas  <br/>-Estado  <br/>-Tareas no están visibles en modo vinculado  <br/> |La funcionalidad completa está habilitada  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Administración de proyectos como listas de tareas de SharePoint
<a name="pj15_Architecture_VisibilityMode"> </a>

Cuando Project Server está asociada con una colección de sitios de SharePoint en SharePoint mantiene el control, las listas de tareas y los archivos de Project Professional 2013 (.mpp) en las bibliotecas de documentos son visibles para el servicio de aplicación de Project, pero SharePoint mantiene el datos para la sincronización de maestros (vea la figura 1). No puede realizarse la programación del servidor con el elemento web de programación. Puede usar Project Professional para sincronizar con y editar la lista de tareas en un sitio de proyecto. A partir de las listas de tareas de SharePoint, las organizaciones pueden evolucionar gradualmente para usar la funcionalidad completa de Project Server.
  
La Figura 1 muestra los siguientes procesos cuando se mantienen los proyectos en las listas de tareas de SharePoint: 
  
- (A) Project Professional puede sincronizarse con las listas de tareas y crear nuevos sitios de proyectos en una recopilación de sitios ya sea antes o después de la asociación con Project Application Service.
    
- (B) Project Server se sincroniza con los datos del sitio del proyecto a fin de informar, pero SharePoint mantiene los datos maestros y las listas de tareas siguen en lectura/escritura.
    
- (C) Después de la asociación, Project Professional puede crear nuevos proyectos y guardar o publicar en Project Server. La caché activa en Project Professional mantiene la sincronización de datos con Project Server.
    
- (D) cuando se publica un nuevo proyecto en Project Professional, el usuario tiene la opción de crear un sitio de proyecto para el proyecto. También se puede crear un proyecto en Project Web App como un tipo de proyecto de lista de tareas de SharePoint o como un tipo de proyecto de empresa de control total (EPT). Paso (D), muestra el EPT de control total.
    
**Figura 1. Utilizar los sitios de proyecto como listas de tareas en SharePoint**

![Uso de sitios de proyecto en modo de visibilidad] (media/pj15_Architecture_VisibilityMode.gif "Uso de sitios de proyecto en modo de visibilidad")

<br/>

### <a name="managing-projects-with-full-control"></a>Administración de proyectos con control total
<a name="pj15_Architecture_ManagedMode"> </a>

Cuando Project Server está asociado a una colección de sitios y tiene control total, Project Server importa las listas de tareas como proyectos de empresa de SharePoint y pueden eliminar cualquier archivo .mpp relacionados. Project Server mantiene los datos maestros para la sincronización de la lista de tareas; las listas de tareas en la colección de sitios se convierten en solo lectura (vea la figura 2). Los proyectos importados pueden modificarse mediante el uso de Project Professional o mediante el uso de Project Web App.
  
> [!NOTE]
> Una vez que Project Server importa un proyecto, el usuario escoge si borrar el proyecto desde el sitio o romper la conexión antes de editar el proyecto. La selección puede realizarse en Project Professional. 
  
La Figura 2 muestra los siguientes procesos cuando Project Server mantiene los proyectos empresariales con control total:
  
- (A) El usuario puede escoger qué sitios de proyecto importa. Project Server importa los sitios de proyecto y de manera opcional elimina los archivos .mpp asociados. La lista de tareas de SharePoint de un proyecto importado se convierte en solo lectura.
    
- (B) después de la asociación, Project Professional crea nuevos proyectos y guarda o se publica en Project Server. La caché activa de Project Professional mantiene la sincronización de datos con Project Server. El elemento web de programación en Project Web App puede hacer la programación del servidor.
    
- (C) cuando se publica un nuevo proyecto en Project Professional, el usuario tiene la opción de crear un sitio de proyecto para el proyecto. Un proyecto también se crean en Project Web App con una EPT de control total y publicado con una lista de tareas de sólo lectura a un sitio de proyecto en la colección de sitios.
    
**Figura 2. Utilizar sitios de proyectos con control total**

![Uso de sitios de proyecto en modo administrado] (media/pj15_Architecture_ManagedMode.gif "Uso de sitios de proyecto en modo administrado")
  
## <a name="general-architecture"></a>Arquitectura general
<a name="pj15_Architecture_General"> </a>

La figura 3 muestra una vista general de la arquitectura de Project Server 2013, incluida la aplicación de servicio de Project, una instancia de Project Web App en un WFE y varias otras aplicaciones de cliente incluidas Project Professional 2013.
  
Puede haber varias instancias de Project Web App que se comunican con la aplicación de servicio de proyecto de back-end. Para una instalación local, el WFE puede estar en un servidor independiente en una granja de servidores de SharePoint, o puede ser en el mismo servidor de SharePoint con la aplicación de servicio de Project. Project Online incluye un WFE, la aplicación de servicio de proyecto y un servidor de flujo de trabajo Manager 1.0 de cliente local o remoto. 
  
**Figura 3. Arquitectura general de Project Server 2013**

![Arquitectura de Project Server] (media/pj15_Architecture_ProjectServiceApp_WFE.gif "Arquitectura de Project Server")

<br/>

Los siguientes comentarios generales se aplican a la Figura 3:
  
- **Project Online:** Puede crear aplicaciones que usan las interfaces CSOM, REST y OData. Un paquete de aplicación también puede instalar a receptores de eventos remotos en un servicio web personalizado en un servidor local, en un servidor de Azure o en Microsoft Azure. Project Online no es compatible con aplicaciones de terceros en las soluciones locales, la interfaz WCF, la interfaz ASMX o controladores de eventos local. 
    
- **Receptores de eventos:** También se pueden llamar a receptores de eventos de los controladores de eventos. Project Online admite el registro de receptores de eventos de Project Server remotos, que se puede usar por una instancia de Project Web App en la nube o por una instalación de Project Server local. Una instalación de Project Server local admite receptores de eventos remotos y los controladores de eventos de plena confianza local. 
    
- **Exploradores:** No existen limitaciones entre exploradores acerca de cómo ver algunas páginas de Project Web App, ya que hay en Project Server 2010. Los siguientes exploradores compatibles para su uso completo con Project Web App: 
    
  - Internet Explorer 8.x (en Windows 7 y versiones anteriores de Microsoft Windows), Internet Explorer 9.x e Internet Explorer 10.x 
  - Firefox 4.x (en Windows, Mac OS-X, y Linux/Unix)
  - Safari 5.x (en Windows y Mac OS-X)
  - Chrome
    
- **Interfaces de programación:** Para las aplicaciones de terceros, Project Online expone la interfaz HTTP/HTTPS (incluidos REST), la interfaz CSOM, un servicio de OData para el CSOM y un servicio de OData para informes. Para las aplicaciones de cliente de terceros que se encuentran en local (en la Intranet), puede usar la interfaz WCF para la interfaz PSI, o puede usar las interfaces REST, OData y CSOM a través de HTTP. Los clientes de Project Web App y Project Professional 2013 usan la interfaz WCF. En una instalación de servidor único, los servicios web, CSOM y REST front-end de ASMX internamente llame a los servicios WCF back-end. 
    
    > [!NOTE]
    > La interfaz ASMX basada en SOAP para los servicios web en PSI sigue estando disponible en Project Server 2013, pero está en desuso. 
  
    El servicio de OData para informes se implementa mediante el servicio de WCF OData.svc interno. Puede obtener el documento de metadatos de servicio para los datos de informes mediante el uso de `https://ServerName/ProjectServerName/_api/ProjectData/$metadata`. 
    
    El servicio de OData para CSOM está diseñado para plataformas como Windows RT, iOS y Android, donde puede usar la interfaz REST con JavaScript en páginas HTML. 
    
    > [!NOTE]
    > Aunque la `$metadata` opción para la **ProjectData** informes de servicio es válido, la `$metadata` opción para el servicio de **ProjectServer** del CSOM se ha eliminado en la versión publicada de Project Server 2013. Para obtener más información acerca de las consultas REST para el CSOM, vea [modelo de objetos de cliente (COM) de Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **Reenviador de PSI:** Acceso mediante programación a la PSI en un WFE independiente circula a través del reenviador de PSI, que incluye un reenviador de WCF y un reenviador de servicio Web. Los clientes que usan la interfaz ASMX tener acceso a la PSI por medio del reenviador de servicio Web. Los clientes que usan la interfaz WCF tener acceso a la PSI por medio del reenviador de WCF. El acceso mediante programación a través de la CSOM, OData y REST se transfiere por medio del reenviador de WCF. 
    
- **Flujos de trabajo:** Flujos de trabajo declarativos (flujos de trabajo que se definen en SharePoint Designer 2013) se descargan a 1,0 de cliente de administrador de flujo de trabajo para el procesamiento. Cliente del Administrador de flujo de trabajo 1.0 puede ejecutar en un servidor independiente de la granja de servidores de SharePoint, en Microsoft Azure en la nube o en un solo equipo de Project Server para realizar pruebas o demostraciones. Los flujos de trabajo codificados que se desarrollan con Visual Studio 2012 se procesan en el tiempo de ejecución de flujo de trabajo dentro de SharePoint, como se muestra en Project Server 2010. Para obtener más información, consulte [Getting started desarrollar flujos de trabajo de Project Server](getting-started-developing-project-server-workflows.md).
    
- **Red perimetral (DMZ):** La figura 3 no muestra que un servidor WFE local se puede aislar mediante un firewall adicional en una red perimetral (también conocida como "zona desmilitarizada" o DMZ). Una red perimetral puede permitir que los clientes de Internet tener acceso a SharePoint y Project Server a través de un firewall. 
    
- **Servicios Web de SharePoint:** La figura 3 no muestra la infraestructura de SharePoint, como la aplicación de servicios Web de SharePoint back-end, que forma parte de SharePoint Server 2013. Al instalar Project Server, la aplicación de servicio de proyecto se agrega a los servicios Web de SharePoint. 
    
El nivel front-end incluye aplicaciones de otros fabricantes, Project Professional y Project Web App. Un explorador muestra ASP.NET 4.0 páginas (.aspx) en Project Web App. Las páginas de Project Web App usan elementos Web de Project Server que se comunican con la PSI y también usan elementos Web de SharePoint estándar. 
  
El nivel intermedio incluye la PSI y la capa de objetos de negocio, que se compone de objetos lógicos que representan las entidades de negocios de Project Server. Las entidades empresariales incluyen proyecto, tarea, recurso, asignación y así sucesivamente. La PSI y el nivel de objeto de negocio están estrechamente y se encuentran en el mismo servidor. Una aplicación cliente llama a la PSI a través de una de las interfaces disponibles, y la interfaz PSI invoca los objetos de negocios. Para mejorar el rendimiento, el cliente Web de Project Server 2013 incluye algunos objetos de negocios para las solicitudes que no se use el sistema de cola de Project Server o requieren el servicio de cálculo de Project. Los objetos de negocios WFE comunican directamente con la base de datos de Project.
  
Los componentes de Project Web App de Project Server utilizan la base de datos de configuración de SharePoint 2013 para el programa de instalación del sitio de proyecto y la base de datos de contenido para contenido del sitio de proyecto, como las listas de tareas, páginas personalizadas, flujos de trabajo, configuración de administración, documentos y listas de problemas, riesgos y compromisos. La configuración de SharePoint y bases de datos de contenido admiten características adicionales de administración de proyectos, como las plantillas de proyecto y áreas de trabajo, listas personalizadas para colaboración en equipo e informes.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App y el WFE
<a name="pj15_Architecture_PWAServer"> </a>

Puede configurar varias instancias de Project Web App en un WFE y varios servidores cliente Web en una intranet corporativa para habilitar la distribución de carga para los clientes de intranet. Cuando una aplicación cliente usa una instancia de Project Web App en un servidor cliente Web independiente, las llamadas PSI se enrutan por medio del reenviador de PSI. El reenviador de PSI (ya sea el reenviador de WCF o el reenviador de servicio Web) realiza las siguientes funciones:
  
- Optimiza las llamadas para la PSI desde clientes remotos.
    
- Distingue entre las llamadas PSI que requieren el servicio de cola de Project Server (Project Server Queue Service) y entre las que no lo necesitan. Los nombres de métodos PSI asincrónicos comienzan con Queue, como **QueueCreateProject**.
    
- Identifica las llamadas PSI que invocan controladores de eventos locales registrados.
    
- Identifica las llamadas PSI que requieren el Servicio de cálculo del proyecto (Project Calculation Service).
    
- Utiliza una caché basada en servidor que funciona con la caché activa del cliente en Project Professional para reducir las llamadas de ida y vuelta en Project Server.
    
Después de SharePoint Server autentica a un usuario de Project Server, el reenviador de PSI envía de manera transparente las solicitudes que utilizan servicios back-end a los servicios PSI en el equipo que ejecuta Project Server. Las solicitudes que no requieren servicios back-end se envían a los objetos de negocios en la instancia local de Project Web App. El reenviador de PSI mejora la escalabilidad, rendimiento y confiabilidad para Project Server de procesamiento a través de la LAN, una WAN y en Project Online.
  
Project Web App se desarrolla con ASP.NET 4.0. Los elementos visuales en los archivos .aspx (HTML, controles de servidor y texto estático) son independientes de la lógica de programación en las clases de código subyacente que se encuentran en ensamblados compilados (archivos .dll). Las páginas de sitio en Project Web App, como la página de nivel superior, el centro de proyectos y el centro de informes, se pueden personalizar mediante el uso de elementos Web. No pueden editarse las páginas de aplicación que no tienen una opción de **Editar página** en el menú **Acciones del sitio** , como la página Configuración del servidor y la página de revisión del parte de horas. 
  
### <a name="the-csom-and-the-project-server-interface"></a>El CSOM y la interfaz de Project Server (Project Server Interface)
<a name="pj15_Architecture_PSI"> </a>

La PSI se calcula en 22 servicios públicos, como **proyectos**, **recursos**, **CustomField**y **estado**. PSI también contiene siete servicios privados para uso interno. La PSI es fundamental API de Project Server; expone la funcionalidad de Project Server para el CSOM y a las aplicaciones externas. El CSOM incluye las clases que tienen acceso a las usadas con más frecuencia clases PSI y miembros que se utilizan para aplicaciones de terceros. En Project Server 2013, algunas funciones de Project Server no está disponible en el CSOM, como los servicios de **administración**, **calendario**, **PortfolioAnalyses**y **seguridad** . 
  
Project Professional 2013 y el uso de Project Web App de la PSI para obtener acceso a datos de Project Server en el borrador, publicado y archiva las tablas y vistas de la base de datos de Project. Puede tener acceso a un servicio de la PSI a través de un archivo de proxy o de un ensamblado de proxy, para los servicios de WCF o los servicios web ASMX.
  
> [!NOTE]
> El CSOM es la interfaz preferida para desarrolladores de Project Server de terceros; se puede usar para aplicaciones que tienen acceso a una instalación de Project Server local y Project Online. Se recomienda usar el CSOM para el desarrollo de nuevas aplicaciones, si el CSOM incluye la funcionalidad que requiere la aplicación. 
  
Algunas aplicaciones de línea de negocio (LOB) y otras aplicaciones de terceros que se desarrollaron para Project Server 2010 requieren servicios PSI que aún no representados en el CSOM. Si tienen como objetivo sólo una instalación local de Project Server, las aplicaciones pueden seguir usando la interfaz WCF o la interfaz ASMX de la PSI.
  
Las aplicaciones cliente llaman a través de servidores proxy de servicio a la PSI. Los clientes que usan la interfaz WCF tener acceso a todos los servicios PSI a través de `https://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc`. Los clientes que usan una interfaz de servicio web ASMX usan la dirección URL de Project Web App para el servicio específico. Por ejemplo, el servicio de **recursos** está en `https://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl`. Si las aplicaciones no tiene acceso a la intranet a Project Server, pueden utilizar un servidor de Project Web App en una red perimetral (no se muestra en la figura 3).
  
La figura 4 se muestra el panel **conexiones** en el **Administrador de Internet Information Services (IIS)** para una instalación de un único servidor de SharePoint Server 2013, Project Server 2013 y un sitio de administración de flujo de trabajo local para 1.0 de cliente del Administrador de flujo de trabajo. La colección de sitios de SharePoint (A) incluye los servicios PSI front-end en el `_vti_bin\PSI` subdirectorio virtual. La aplicación de servicios Web de SharePoint (B) incluye la aplicación de servicio de Project, con los servicios PSI back-end en el `508c23fb7dfd4c83a8919fae24bc68c5/PSI` subdirectorio virtual. El GUID es el nombre de la instancia de aplicación de servicio de proyecto para esa instalación de Project Server. 
  
**Figura 4. Administrador de Internet Information Services (IIS) que muestra la PSI front-end (A) y la PSI back-end (B)**

![La PSI front-end y back-end PSI] (media/pj15_Architecture_PSI_IIS.gif "La PSI front-end y back-end PSI")
  
Las aplicaciones cliente no pueden tener acceso directamente a los servicios de WCF para la PSI en la aplicación de servicio de proyecto de back-end. Si no requieren acceso a Project Online, las aplicaciones cliente y los componentes de las aplicaciones LOB usan a servidores proxy para la interfaz PSI. Una dirección URL de back-end para la interfaz WCF del **recurso de** servicio en la figura 4, por ejemplo, podría ser `https://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. Puerto 32843 es el puerto HTTP predeterminado para la aplicación de servicios Web de SharePoint (32844 es el puerto de comunicaciones HTTPS). Sin embargo, el archivo web.config para los bloques de Project Web App de acceso directo a los servicios PSI back-end.
  
> [!NOTE]
> La descarga del SDK de Project 2013 incluye archivos de proxy PSI para los servicios de WCF y los servicios ASMX así como instrucciones acerca de cómo compilarlos en ensamblados de servidores proxy. > Para crear archivos proxy PSI que usan la interfaz WCF, se debe usar la utilidad svcutil.exe o Visual Studio directamente en el equipo de Project Server. 
  
Normalmente, los miembros de los servicios de PSI producen o consuman objetos **DataSet con** tipo como los medios para intercambiar información con los objetos de negocios. También hay varios modelos diferentes para el desarrollo de PSI. Por ejemplo, los servicios PSI **LookupTable** , **CustomFields**y **recursos**utilizan objetos de filtro XML para la manipulación de **conjunto de datos** y otros servicios no; Algunos métodos en el servicio de **estado de** usan de un parámetro de _changeXml_ , mientras que otros métodos y servicios que no. El CSOM no usa conjuntos de datos. Aunque el CSOM tiene un modelo de programación diferente de la PSI, y puede usar los ensamblados de .NET o JavaScript, desarrollo con el CSOM es generalmente más sencilla y más coherente que el desarrollo con la PSI. 
  
Para obtener más información acerca de la interfaz PSI, vea [Descripción general de referencia de PSI de Project](project-psi-reference-overview.md). Para obtener más información sobre el CSOM, vea [modelo de objetos de cliente (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Objetos de negocio en WFE y la aplicación de servicio de Project
<a name="pj15_Architecture_BusinessObjects"> </a>

El modelo de objeto interno de Project Server incluye los objetos de negocio, que representan a las entidades lógicas como Proyecto y Recurso. Las aplicaciones de cliente acceden a los objetos de negocio tan solo a través de CSOM o la PSI. Los objetos de negocio, sin embargo, acceden a las tablas y vistas de borrador, publicadas y de archivo en la base de datos de Project.
  
Los objetos de negocio no se exponen a desarrolladores de terceros. La PSI controla la asignación de API a los objetos de negocio y el CSOM asigna su API al PSI. Las entidades lógicas de los objetos de negocio pueden clasificarse en tres tipos:
  
- **Las entidades principales** son objetos como proyectos, tareas, asignaciones, recursos y calendarios. Las entidades centrales incluyen lógica de negocios básica como permisos y normas de nomenclatura. 
    
- **Las entidades de negocio** son objetos como partes de horas, carteras de proyectos y modelos. Las entidades de negocio incluyen lógica empresarial adicional y normalmente se suelen crear a partir de una combinación de entidades principales. 
    
- **Las entidades de soporte técnico** son objetos como seguridad y validación. 
    
En Project Server 2010, todos los objetos de negocio se implementan en la aplicación de servicio de Project. En Project Server 2013, el WFE hospeda muchos de los objetos de negocios que procesan los métodos sincrónicos y no requieren el servicio de cálculo de Project. Los métodos PSI sincrónicos, como **DeleteProject** y **ReadAssignments** no utilizan el servicio de cola de Project Server. Métodos asincrónicos de la PSI tienen nombres que empiezan con `Queue`, como **QueueCreateProject** y **QueueUpdateTimesheet**. Un método asincrónico, envía un mensaje para el servicio de cola de Project Server, que programa el procesamiento del método mientras el control se devuelve al usuario.
  
El reenviador de PSI determina qué solicitudes se envían a la aplicación del servicio de Project y cuáles pueden ser procesados por los objetos de negocio en WFE. Estos objetos desvían la aplicación de servicio de Project y tienen acceso directo a la base de datos de Project, de una manera similar a la que otros procesos de SharePoint acceden directamente en un WFE a la configuración y bases de datos de contenido. La ejecución de muchos objetos de negocio en el WFE mejora la eficiencia de Project Server, reduce la carga en el nivel de la aplicación y permite a Project Server realizar una mejor ampliación para el aumento de las cargas de trabajo.
  
> [!NOTE]
> En Project Server 2013, los controladores de eventos local deben implementarse en el WFE y en el equipo de Project Server de back-end. 
  
### <a name="project-server-database"></a>Base de datos de Project Server
<a name="pj15_Architecture_DAL"> </a>

En Project Server 2013, las cuatro bases de datos de Project Server de versiones anteriores se combinan en una base de datos de Project en SQL Server. El nombre de base de datos del proyecto de forma predeterminada es ProjectService. Las tablas y vistas de informes conservan sus nombres anteriores con el `dbo` prefijo, como dbo. MSP_EpmProject y dbo. MSP_EpmProject_UserView. Las tablas y vistas que había anteriormente en la base de datos de borrador tienen la `draft` prefijo. Las tablas y vistas de la base de datos publicados tienen la `pub` prefijo. Las tablas y vistas de la base de datos de archivo tienen la `ver` prefijo. 
  
> [!IMPORTANT]
> Dirigir acceso no es compatible con el borrador ( `draft` prefijo), publicado ( `pub` prefijo) y de archivo ( `ver` prefijo) tablas y vistas. Deben usar informes sólo las tablas y vistas, que tienen informes la `dbo` prefijo. 
  
Los datos de Project Server están divididos en la base de datos de Project como se indica a continuación:
  
- Las tablas de borrador y vistas contienen datos de proyectos no publicados que se crearon por Project Professional y otras aplicaciones. Project Web App no muestra los datos del proyecto de las tablas de borrador y vistas.
    
- Las vistas y tablas publicadas contienen todos los proyectos publicados y recursos de empresa, datos globales para tipos de proyecto empresarial (EPT) y otras plantillas de proyecto. Los proyectos publicados son visibles en Project Web App. Los datos publicados también incluyen las tablas que son específicas de Project Web App (partes de horas, modelos, vistas etc.) y las tablas de datos globales (campos personalizados, las tablas de búsqueda, los permisos de autorización de Project Server y metadatos).
    
- Los datos de archivo guardan las versiones de copia de seguridad de los proyectos, recursos, campos personalizados y otros datos.
    
- Los datos de informes se pueden usar para el acceso de sólo lectura en las aplicaciones de terceros y para los informes. Cubos de OLAP Server Project usar las vistas Informes que tienen la `_OlapView` sufijo. Cubos OLAP están disponibles en una instalación de Project Server local, pero no están disponibles en Project Online. 
    
    Los datos de informes son exhaustivos y se actualizan prácticamente en tiempo real. Las tablas y vistas de informes están optimizadas para la generación de informes de solo lectura. Así, por ejemplo, las tablas de informes están desnormalizadas para ofrecer datos redundantes y para reducir el número de tablas relacionales.
    
Las entidades lógicas como Recurso o Proyecto pueden abarcar varias tablas y todas las tablas de una entidad determinada tienen la misma clave principal. La clave principal es un GUID en una sola columna que identifica únicamente una instancia de una entidad particular.
  
Datos de Project Server para cada instancia de Project Web App se almacenan en una base de datos de proyecto independiente con un nombre diferente. Las aplicaciones de cliente que tienen acceso directo a Project Server pueden leer directamente las tablas y vistas de informes. Para el acceso remoto, aplicaciones cliente pueden utilizar la interfaz de OData y la interfaz de REST para obtener los datos de informes. Los clientes deben usar sólo el CSOM o la PSI para tener acceso el borrador, publicado y archivar las tablas y vistas. El servicio de datos de informes (RDS, que no se muestra en la figura 3) actualiza los datos de informes de datos publicados, casi en tiempo real. La base de datos de proyecto puede estar ubicada en un servidor independiente.
  
Esquemas se documentan sólo para las tablas y vistas de informes. Para una instalación de Project Server local, puede agregar informes tablas y vistas para las entidades que no están definidas en el esquema de base de datos de Project. También puede crear bases de datos independientes para las aplicaciones personalizadas local. Modificación no es compatible con el borrador, publicados y archiva las tablas y vistas. Debido a que la base de datos del proyecto no es directamente accesible en Project Online, informes de tablas y vistas no se pueden modificar. Sin embargo, si tiene una cuenta de SQL Azure, puede crear bases de datos independientes para su uso personalizado con Project Online.
  
### <a name="event-receivers"></a>Receptores de eventos
<a name="pj15_Architecture_EventHandlers"> </a>

Controladores de eventos locales y receptores de eventos remotos para Project Server habilitar la extensibilidad de terceros en respuesta a eventos de Project Server como la creación o publicación de un proyecto. En Project Server 2010, todos los controladores de eventos son locales y se escriben en el código de plena confianza, implementan directamente en el equipo que ejecuta Project Server y a los servidores cliente Web y se ejecutan en el sistema de eventos de Project Server. Debido a que Project Online no se puede usar controladores de eventos de plena confianza, Project Server 2013 implementa receptores de eventos remotos que son similares a los receptores de eventos remotos en SharePoint Server 2013. Una instalación local de Project Server 2013 puede usar controladores de eventos de plena confianza tradicional y receptores de eventos remotos.
  
Un receptor de eventos remotos de Project Server puede implementarse en un servicio web personalizado con un extremo de SOAP que se ejecuta en Microsoft Azure u otros entornos que admiten servicios web SOAP. Un paquete de la aplicación Project Server puede incluir receptores de eventos remotos que se instalan con la aplicación.
  
Receptores de eventos remotos pueden devolver la llamada en Project Server mediante el uso de los extremos CSOM (no se muestra en la figura 3). La llamada a un receptor de eventos remotos incluye información desde el sistema de eventos de Project Server y la instancia de Project Web App (o el inquilino de Project Web App en Project Online) que emite la llamada. Receptores de eventos remotos permiten crear y hospedar un solo servicio web que se puede usar varias instalaciones de Project Server. Por el contrario, se deben implementar controladores de eventos de plena confianza local en cada instalación de Project Server.
  
### <a name="publishing-and-server-side-scheduling"></a>Publicación y programación del servidor
<a name="pj15_Architecture_PublishingScheduling"> </a>

Project Server 2013 es compatible con ambas actualizaciones de programación de proyecto manuales y automatizadas. El proceso predeterminado es una actualización de programación manual. Es decir, el jefe de proyecto desprotege y abre un proyecto en Project Professional o Project Web App, aplica los cambios y, a continuación, guarda y publica el proyecto para que los cambios estén disponible para todos los usuarios. Project Professional tiene un motor de programación que calcula los cambios y, a continuación, guarda los cambios en Project Server. En Project Server 2010, el motor de programación del lado del servidor es una implementación diferente desde el motor de programación de Project Professional.
  
En Project Server 2013, el servicio de cálculo de Project implementa el mismo motor de programación que se encuentra en Project Professional 2013. El servicio de cálculo de Project se ejecuta en un servicio de Windows denominado **Servicio de cálculo de Microsoft Project Server**. Edición de una programación de proyecto en Project Web App o con aplicaciones de terceros que utilizan los resultados CSOM en exactamente el mismo cambios en la programación que harían que Project Professional.
  
> [!NOTE]
> Las aplicaciones de terceros que usan la PSI pueden mostrar algunas diferencias de programación de una programación que calcula Project Web App. Para compatibilidad con versiones anteriores, los métodos públicos de PSI que realice sigue la programación del servidor usan el motor de programación que se introdujo en Project Server 2010. Una excepción es **QueueUpdateProject2**, que es un nuevo método PSI de Project Server 2013. Por ejemplo, el motor de programación más antiguos no programa subproyectos ni vínculos a otros proyectos y no calcula los campos de valor acumulado. Para evitar posibles de programación de las diferencias entre las aplicaciones de terceros y Project Professional o Project Web App, debe desarrollar las aplicaciones con el CSOM siempre que sea posible. 
  
Project Server permite la versión publicada de un proyecto para que se actualice mientras un jefe de proyecto utiliza la versión de borrador, siguiendo las instrucciones siguientes:
  
1. Project Server aplica las actualizaciones y reprograma la versión publicada.
    
2. Project Server guarda la actualización para aplicarla a la versión de borrador en caso de que ocurra alguno de los siguientes eventos:
    
   - Project Professional abre el proyecto.
    
   - Project Professional intenta publicar el proyecto.
    
3. En caso de que surja un conflicto, el jefe de proyecto recibe una notificación y debe resolver el conflicto antes de que se publique la versión de borrador.
    
## <a name="see-also"></a>Vea también

- [Información general de Project 2013 para desarrolladores](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Programación de Project Server](project-server-programmability.md)  
- [Modelo de objetos de cliente (COM) de Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [Lo que hace y no hace PSI](what-the-psi-does-and-does-not-do.md)  
- [Empezar a desarrollar flujos de trabajo de Project Server](getting-started-developing-project-server-workflows.md)   
- [Información general de referencia PSI de Project](project-psi-reference-overview.md)   
- [Protocolo de datos abierto](https://www.odata.org/)
    

