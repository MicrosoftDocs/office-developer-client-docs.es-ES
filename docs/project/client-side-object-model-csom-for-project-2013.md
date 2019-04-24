---
title: Modelo de objetos de cliente (CSOM) para Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: El modelo de objetos de cliente (CSOM) de Project Server 2013 implementa la funcionalidad de servidor común. El modelo de objetos de cliente de Project Server incluye un CSOM de Microsoft. NET, un CSOM de Microsoft Silverlight, un CSOM de Windows Phone 8 y un modelo de objetos de JavaScript (JSOM). Además, el CSOM incluye un servicio OData que habilita una interfaz REST. La interfaz REST va dirigida principalmente al desarrollo de aplicaciones en plataformas que no son de Windows, como iOS y Android.
localization_priority: Priority
ms.openlocfilehash: b722e316f5cb2054eb6522297c5c5ef3e75f9fa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355205"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Modelo de objetos de cliente (CSOM) para Project 2013

El modelo de objetos de cliente (CSOM) de Project Server 2013 implementa la funcionalidad de servidor común. El modelo de objetos de cliente de Project Server incluye un CSOM de Microsoft. NET, un CSOM de Microsoft Silverlight, un CSOM de Windows Phone 8 y un modelo de objetos de JavaScript (JSOM). Además, el CSOM incluye un servicio OData que habilita una interfaz REST. La interfaz REST va dirigida principalmente al desarrollo de aplicaciones en plataformas que no son de Windows, como iOS y Android.
  
> [!NOTE]
> Las soluciones de Project Online deben utilizar el modelo de objetos de cliente. Sin embargo, con las aplicaciones locales puede usar el CSOM o la interfaz de Project Server (PSI). Si el CSOM incluye la funcionalidad que va a usar, se recomienda usarlo para las nuevas aplicaciones. 
  
En las extensiones de CSOM, el objeto **ProjectContext** proporciona el punto de entrada al contenido y las funciones del servidor. El CSOM .NET, el CSOM Silverlight y el CSOM de Windows Phone usan el objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx); el JSOM usa el objeto **PS. ProjectContext**. Las propiedades **ProjectContext** proporcionan acceso directo a los objetos principales de Project Server en la colección de sitios actual de Project Web App. Para obtener información acerca de la ubicación de los ensamblados de CSOM y el archivo de JavaScript, vea [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 **El modelo de seguridad y las aplicaciones** Las aplicaciones deben usar el CSOM para las operaciones CRUD (crear, leer, actualizar y eliminar) con Project Server 2013 y Project Online. Las aplicaciones de proyecto no usan el modelo de autenticación solo de aplicación en SharePoint 2013. Una aplicación de Project Server requiere un ámbito de solicitud de permisos específicos que especifica en el nombre de quién se ejecutan los comandos. 
  
 **Consultas REST** Puede crear consultas REST del servicio OData de CSOM sin consumir los metadatos. Algunas herramientas de terceros habilitan el uso de los ensamblados de .NET para el CSOM para desarrollar aplicaciones para otros dispositivos. Por ejemplo, realice la siguiente búsqueda en Internet: "herramientas de desarrollo multiplataforma de .NET para iOS o Android". 
  
> [!NOTE]
> Aunque la opción `$metadata` para el servicio de informes **ProjectData** es válida ( `https://ServerName/pwaName/_api/ProjectData/$metadata`), la opción `$metadata` para el servicio **ProjectServer** del CSOM se elimina de la versión publicada de Project Server 2013. Para encontrar los objetos y los miembros CSOM que están disponibles como puntos de conexión REST, vea la [biblioteca de JavaScript y la referencia REST para Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Para ver las entidades disponibles en el CSOM a través de la interfaz REST, puede usar la consulta `https://ServerName/pwaName/_api/ProjectServer`. Para las consultas REST, la entidad **ProjectServer** refleja estrechamente propiedades del objeto [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) en el ensamblado administrado de Microsoft.ProjectServer.Client.dll y el objeto [PS. ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) del JSOM. Por ejemplo, puede usar el explorador para obtener información del CSOM sobre proyectos en Project Web App, las tareas de un proyecto específico y el nombre de tarea de una tarea concreta para un recurso especificado, usando las siguientes consultas (cada consulta usa la mismo prefijo de URL  `https://ServerName/pwaName/_api`). Los GUID son valores de ejemplo de **Project.Id**, **EnterpriseResource.Id** y **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

A diferencia de la interfaz de OData para el servicio **ProjectData**, que es de solo lectura para los informes, puede realizar operaciones CRUD con consultas REST con el servicio **ProjectServer**. Las consultas REST para el CSOM de Project Server están diseñadas principalmente para plataformas distintas del escritorio de Windows, como Windows RT, iOS y Android. Para las plataformas de escritorio y servidores Windows, como Windows 7, Windows 8 y Windows Server 2008 R2, puede usar los ensamblados administrados de CSOM. Para las aplicaciones web, puede usar PS.js para JavaScript. Para obtener información acerca de las operaciones CRUD con consultas REST, consulte el artículo [Usar operaciones de consulta de OData en solicitudes REST de SharePoint](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) en el SDK de SharePoint 2013. Para obtener información sobre el uso del servicio **ProjectData**, consulte [Consulta de fuentes OData de datos de informes de Project](https://msdn.microsoft.com/library/office/jj163048.aspx).
  
La tabla 1 enumera las propiedades **ProjectContext** que representan los objetos de Project Server. Puede usar estos objetos para recuperar otras entidades de Project Server 2013, como tareas. 
  
**Tabla 1. Propiedades de ProjectContext que proporcionan acceso a los objetos de Project Server en el CSOM y el JSOM**

|**CSOM (.NET, Silverlight y Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Events](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |eventos  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Phases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |fases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |proyectos  <br/> |
|[Stages](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |etapas  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>En esta sección

[Getting started with the Project Server CSOM and .NET](getting-started-with-the-project-server-csom-and-net.md) proporciona información general sobre .NET y el CSOM de Project Server, instrucciones sobre cómo crear una simple extensión del CSOM de .NET en Visual Studio 2012 y ejemplos de códigos de ayuda. 
  
[Getting started with the Project Server 2013 JavaScript object model](getting-started-with-the-project-server-2013-javascript-object-model.md) proporciona información general sobre el JSOM de Project Server, instrucciones sobre cómo crear una simple extensión de JSOM en Visual Studio 2012 y ejemplos de códigos de ayuda. 
  
Consulte también estos artículos que muestran cómo usar el CSOM:
  
- [Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Trabajar con proyectos con el modelo de objetos JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> También puede usar Visual Studio 2010 para el desarrollo de .NET Framework 4 con el CSOM. 
  
## <a name="reference"></a>Referencia

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Vea también



[Project Server 2013 architecture](project-server-2013-architecture.md)


[Elegir el conjunto de API correcto en SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

