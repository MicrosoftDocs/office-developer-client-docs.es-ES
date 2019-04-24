---
title: Referencia de la biblioteca y REST de JavaScript para Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: La referencia de la biblioteca y REST de JavaScript para Project Server 2013 contiene información sobre el modelo de objetos de JavaScript y la interfaz de REST que usa para obtener acceso a la funcionalidad de Project Server. Puede usar estas API para desarrollar aplicaciones web entre exploradores, Complementos de Project Professional 2013 y aplicaciones para dispositivos que no son Windows y que tienen acceso a Project Server 2013 y Project online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358110"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Referencia de la biblioteca y REST de JavaScript para Project Server

La referencia de la biblioteca y REST de JavaScript para Project Server 2013 contiene información sobre el modelo de objetos de JavaScript y la interfaz de REST que usa para obtener acceso a la funcionalidad de Project Server. Puede usar estas API para desarrollar aplicaciones web entre exploradores, Complementos de Project Professional 2013 y aplicaciones para dispositivos que no son Windows y que tienen acceso a Project Server 2013 y Project online.
  
> [!NOTE]
> El modelo de objetos de JavaScript y la interfaz REST se alinean con el modelo de objetos del lado cliente (CSOM) de Project Server. Proporcionan una funcionalidad equivalente al espacio de nombres **Microsoft. ProjectServer. Client** en el CSOM. 
  
Puede acceder a la funcionalidad de Project Server a través del modelo de objetos de JavaScript, [](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) que se define en `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` el espacio de nombres PS del archivo. El objeto [ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) del espacio de nombres [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) es el punto de entrada al modelo de objetos de JavaScript. 
  
> [!NOTE]
> Para examinar el modelo de objetos de JavaScript y ayudar con la depuración, puede usar el archivo PS. Debug. js en el mismo directorio. Para ayudar con el desarrollo en un equipo remoto, la [descarga del SDK de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435) incluye los ensamblados de .NET Framework para el CSOM y los archivos PS. js y PS. Debug. js. 
  
También puede obtener acceso a la funcionalidad de Project Server a través de la interfaz REST. El punto de entrada a la interfaz REST es el recurso **ProjectServer** , al que se obtiene acceso `https://ServerName/pwaName/_api/ProjectServer` mediante el URI del extremo. Por ejemplo, la siguiente consulta obtiene las asignaciones del proyecto especificado (Reemplace _ServerName_ y _pwaName_, y cambia el GUID para que sea igual a un proyecto).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

El recurso **ProjectServer** se describe en [recursos de ProjectServer en la interfaz de REST](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Otros recursos de REST se describen en la documentación de los objetos y miembros de JavaScript correspondientes en esta referencia. Para obtener más información sobre el uso de REST, vea [modelo de objetos de cliente (CSOM) para Project Server](client-side-object-model-csom-for-project-2013.md) y [programación con el servicio SharePoint 2013 Rest](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Referencia de la biblioteca y REST de JavaScript para Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Referencia de REST y biblioteca de JavaScript de PS. js](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contiene información sobre el modelo de objetos de JavaScript y la interfaz de REST para Project Server 2013. 
    
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Documentación para desarrolladores de Project 2013](project-2013-developer-documentation.md)   
- [Modelo de objetos de cliente (CSOM) para Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Introducción al modelo de objetos de JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Trabajar con proyectos con el modelo de objetos JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

