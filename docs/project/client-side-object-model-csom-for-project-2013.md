---
title: Modelo de objetos de cliente (COM) de Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: El modelo de objetos de cliente (COM) de Project Server 2013 implementa la funcionalidad del servidor comunes. CSOM de Project Server incluye un Microsoft .NET CSOM, un Microsoft Silverlight CSOM, un CSOM de Windows Phone 8 y un modelo de objetos de JavaScript (JSOM). Además, el CSOM incluye un servicio de OData que permite una interfaz de REST. La interfaz REST está pensada principalmente para el desarrollo de aplicaciones en plataformas que no son de Windows, como iOS y Android.
ms.openlocfilehash: a17dc816cd2033ff0057821ef029f0163881f9ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821295"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Modelo de objetos de cliente (COM) de Project 2013

El modelo de objetos de cliente (COM) de Project Server 2013 implementa la funcionalidad del servidor comunes. CSOM de Project Server incluye un Microsoft .NET CSOM, un Microsoft Silverlight CSOM, un CSOM de Windows Phone 8 y un modelo de objetos de JavaScript (JSOM). Además, el CSOM incluye un servicio de OData que permite una interfaz de REST. La interfaz REST está pensada principalmente para el desarrollo de aplicaciones en plataformas que no son de Windows, como iOS y Android.
  
> [!NOTE]
> Soluciones para Project Online deben usar el CSOM. Sin embargo, las aplicaciones locales pueden usar el CSOM o Project Server Interface (PSI). Si el CSOM incluye la funcionalidad que se va a utilizar, se recomienda que use CSOM para aplicaciones nuevo. 
  
En las extensiones CSOM, el objeto de **ProjectContext** proporciona el punto de entrada a contenido de servidor y la funcionalidad. El CSOM de .NET, el CSOM de Silverlight y el CSOM de Windows Phone, use el objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) y el JSOM usa el **PS. ProjectContext** objeto. Propiedades de **ProjectContext** proporcionan acceso directo a los objetos de Project Server core en la colección de sitios actual de Project Web App. Para obtener información acerca de la ubicación de los ensamblados CSOM y el archivo JavaScript, consulte [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 **Aplicaciones y el modelo de seguridad** Aplicaciones deben usar el CSOM para CRUD (crear, leer, actualizar, eliminar) operaciones con Project Server 2013 y Project Online. Aplicaciones de Project no use el modelo de autenticación solo de aplicación en SharePoint 2013. Una aplicación de Project Server requiere un ámbito de solicitud de permisos específicos que se especifica en cuyo nombre se va a ejecutar comandos. 
  
 **Consultas de REST** Puede crear consultas REST del servicio OData CSOM sin consumir los metadatos. Algunas herramientas de terceros permiten el uso de los ensamblados de .NET para el CSOM para desarrollar aplicaciones para otros dispositivos. Por ejemplo, buscar en Internet "multiplataforma .NET herramientas de desarrollo para iOS o Android." 
  
> [!NOTE]
> Aunque la `$metadata` opción para la **ProjectData** informes de servicio es válido ( `http://ServerName/pwaName/_api/ProjectData/$metadata`), la `$metadata` opción para el servicio de **ProjectServer** del CSOM se ha eliminado en la versión publicada de Project Server 2013. Para buscar los objetos CSOM y miembros que están disponibles como extremos REST, consulte la [biblioteca de JavaScript y referencia REST para Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Para ver las entidades disponibles en el CSOM a través de la interfaz de REST, puede usar el `http://ServerName/pwaName/_api/ProjectServer` consulta. Para las consultas REST, la entidad **ProjectServer** refleja estrechamente las propiedades del objeto de [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) en el ensamblado Microsoft.ProjectServer.Client.dll administrados y la [PS. ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) objeto en el JSOM. Por ejemplo, puede usar el explorador para obtener información desde el CSOM acerca de los proyectos en Project Web App, las asignaciones en un proyecto especificado y el nombre de la tarea de una asignación especificada para un recurso especificado mediante el uso de las siguientes consultas (cada consulta usa el mismo `http://ServerName/pwaName/_api` prefijo de dirección URL). Los GUID son valores de ejemplo para **Project.Id**, **EnterpriseResource.Id**y **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

A diferencia de la interfaz de OData para el servicio **ProjectData** , que es de sólo lectura para informes, se pueden realizar operaciones CRUD con consultas de REST con el servicio de **ProjectServer** . Consultas de REST para el CSOM de Project Server se han diseñado principalmente para plataformas que no sea el escritorio de Windows, como Windows RT, iOS y Android. Para las plataformas de escritorio y servidor de Windows, como Windows 7, Windows 8 y Windows Server 2008 R2, puede usar los ensamblados CSOM administrado. Para las aplicaciones web, puede usar PS.js para JavaScript. Para obtener información acerca de cómo realizar operaciones CRUD con consultas de REST, vea el tema de [las operaciones de consulta de uso OData en solicitudes REST de SharePoint](http://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) en el SDK de SharePoint 2013. Para obtener información acerca de cómo utilizar el servicio **ProjectData** , vea [fuentes de OData consultar datos de informes del proyecto](https://msdn.microsoft.com/en-us/library/office/jj163048.aspx).
  
La tabla 1 se enumeran las propiedades de **ProjectContext** que representan objetos de Project Server. Puede usar estos objetos para recuperar otras entidades de Project Server 2013, como las asignaciones y tareas. 
  
**Tabla 1. Propiedades de ProjectContext que brindan acceso a objetos de Project Server en el CSOM y JSOM**

|**CSOM (.NET, Silverlight y Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[Controladores de eventos](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |controladores de eventos  <br/> |
|[Eventos](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[Tablas de búsqueda](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |tablas de búsqueda  <br/> |
|[Fases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |proyectos  <br/> |
|[Etapas](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>En esta sección

[Getting started con Project Server CSOM y .NET](getting-started-with-the-project-server-csom-and-net.md) proporciona información general sobre el CSOM de Project Server y. NET, instrucciones sobre cómo crear una simple extensión del CSOM de .NET en Visual Studio 2012 y ejemplos de códigos admitidos. 
  
[Getting started with el modelo de objetos de JavaScript de Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) proporciona información general sobre el JSOM de Project Server, instrucciones sobre cómo crear una simple extensión JSOM en Visual Studio 2012 y ejemplos de códigos admitidos. 
  
Además, debe desproteger estos artículos que muestran cómo usar el CSOM:
  
- [Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Trabajar con proyectos con el modelo de objetos JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> También puede usar Visual Studio 2010 para el desarrollo de .NET Framework 4 con el CSOM. 
  
## <a name="reference"></a>Referencia

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Vea también



[Project Server 2013 architecture](project-server-2013-architecture.md)


[Elegir el conjunto de API correcto en SharePoint 2013](http://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

