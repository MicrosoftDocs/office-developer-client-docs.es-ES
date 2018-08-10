---
title: Biblioteca de JavaScript y referencia REST para Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: La biblioteca de JavaScript y REST de referencia para Project Server 2013 contiene información sobre el modelo de objetos de JavaScript y la interfaz REST que use para tener acceso a funciones de Project Server. Puede usar estas API para desarrollar aplicaciones web entre exploradores, Project Professional 2013 complementos y aplicaciones para dispositivos que no son de Windows que tienen acceso a Project Server 2013 y Project Online.
ms.openlocfilehash: f834ffdc80de28eceb2d7ab9b30c1444b0478bd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821321"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Biblioteca de JavaScript y referencia REST para Project Server

La biblioteca de JavaScript y REST de referencia para Project Server 2013 contiene información sobre el modelo de objetos de JavaScript y la interfaz REST que use para tener acceso a funciones de Project Server. Puede usar estas API para desarrollar aplicaciones web entre exploradores, Project Professional 2013 complementos y aplicaciones para dispositivos que no son de Windows que tienen acceso a Project Server 2013 y Project Online.
  
> [!NOTE]
> El modelo de objetos de JavaScript y la interfaz REST de alinean con el modelo de objetos de cliente (COM) de Project Server. Proporcionan una funcionalidad equivalente al espacio de nombres **Microsoft.ProjectServer.Client** en el CSOM. 
  
Puede obtener acceso a funciones de Project Server mediante el modelo de objetos de JavaScript, que se define en el espacio de nombres [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) en el `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` archivo. El objeto de [ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) en el espacio de nombres [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) es el punto de entrada para el modelo de objetos de JavaScript. 
  
> [!NOTE]
> Para examinar el modelo de objetos de JavaScript y ayuda con la depuración, puede usar el archivo PS.debug.js en el mismo directorio. Para ayudar con el desarrollo en un equipo remoto, el [SDK de Project 2013 descargar](https://www.microsoft.com/en-us/download/details.aspx?id=30435) incluye los ensamblados de .NET Framework para el CSOM y los archivos PS.js y PS.debug.js. 
  
También puede tener acceso a funciones de Project Server a través de la interfaz de REST. El punto de entrada a la interfaz de REST es el recurso **ProjectServer** , que se accede mediante el uso de la `http://ServerName/pwaName/_api/ProjectServer` URI del extremo. Por ejemplo, la siguiente consulta obtiene las asignaciones en el proyecto especificado (reemplace _ServerName_ y _pwaName_y cambiar el GUID para que coincida con un proyecto).
  
`http://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

El recurso de **ProjectServer** se describe en [ProjectServer recursos en la interfaz de REST](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Otros recursos REST se describen en la documentación para los objetos de JavaScript correspondientes y miembros en esta referencia. Para obtener más información acerca del uso de REST, vea [modelo de objetos de cliente (COM) de Project Server](client-side-object-model-csom-for-project-2013.md) y [el servicio REST de SharePoint 2013 de programación](http://msdn.microsoft.com/en-us/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Biblioteca de JavaScript y referencia REST para Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Referencia REST y la biblioteca de PS.js JavaScript](http://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contiene información sobre el modelo de objetos de JavaScript y la interfaz de REST para Project Server 2013. 
    
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Documentación para desarrolladores de Project 2013](project-2013-developer-documentation.md)   
- [Modelo de objeto de cliente (CSOM) para Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Introducción al modelo de objetos JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Trabajar con proyectos con el modelo de objetos JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

