---
title: Complementos de panel de tareas para Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 y Project Professional 2013 tanto el panel de tareas de soporte técnico de complementos de Office. Puede usar complementos de panel de tareas para integrar datos de proyectos, tareas, recursos y vistas en un proyecto con otras aplicaciones cliente de Office 2013, aplicaciones de SharePoint, elementos Web, otras páginas web y datos externos.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330019"
---
# <a name="task-pane-add-ins-for-project"></a>Complementos del Panel de tareas de Project

Project Standard 2013 y Project Professional 2013 tanto el panel de tareas de soporte técnico de complementos de Office. Puede usar complementos de panel de tareas para integrar datos de proyectos, tareas, recursos y vistas en un proyecto con otras aplicaciones cliente de Office 2013, aplicaciones de SharePoint, elementos Web, otras páginas web y datos externos.
  
Los complementos de Office son un modelo de extensibilidad que se admite en varias aplicaciones cliente de Office 2013. La plataforma de complementos completa incluye tipos de complementos contextuales, de contenido y de panel de tareas. Outlook 2013 admite complementos de correo, que pueden mostrar una página web dentro de un mensaje de correo electrónico o un elemento de cita de calendario que está relacionado con el contenido del elemento. Word 2013 y Excel 2013 admiten complementos de contenido, que pueden mostrar una página web como contenido incrustado en un documento. Word 2013, Excel 2013 y Project Professional 2013 admiten complementos de panel de tareas, que pueden mostrar una página web en un panel de tareas donde el contenido está relacionado con la información contextual del proyecto.
  
Por ejemplo, un complemento de Project puede resumir datos en el proyecto activo y Mostrar datos adicionales sobre una tarea o recurso seleccionado. Los datos relacionados en el complemento pueden provenir de un origen externo como una lista de SharePoint, tablas de informes de la base de datos de Project Server, un servicio Web u otra aplicación empresarial. Se puede desarrollar un complemento de panel de tareas con HTML 5, JavaScript, JQuery y otras bibliotecas de JavaScript. Un complemento de panel de tareas no admite directamente los componentes ActiveX, Silverlight o Flash. Aunque un complemento de Office puede usar un elemento **iframe** para obtener acceso a una aplicación web del lado servidor que usa ASP.net y la biblioteca de .net Framework 4,5, este tipo de solución no se recomienda o no se admite. El complemento se puede desarrollar para guardar los datos de forma local o escribir datos en una ubicación externa. 
  
> [!NOTE]
> Los complementos de Project de panel de tareas pueden obtener acceso a los datos de Project online mediante la autenticación OAuth. Con Project Professional 2013, puede desarrollar complementos de panel de tareas que tengan acceso a instalaciones locales de Project Server 2013 y locales o SharePoint 2013 en línea. Por ejemplo, vea [conectar un complemento de panel de tareas de Project a PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) en el blog de Project Programmibility. > Project Standard 2013 no admite la integración directa con datos de Project Server o listas de tareas de SharePoint que se sincronizan con Project Server. 
  
Para obtener más información sobre los complementos para Office 2013, vea complementos de [Office y SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Desarrollo de complementos de panel de tareas

La documentación para desarrolladores de Office y SharePoint Add-Ins incluye artículos y referencias completos. Para obtener una introducción al desarrollo de complementos para Project Professional 2013 y otras aplicaciones cliente de Office 2013 y para la referencia de JavaScript y la referencia de manifiesto XML, consulte [Complementos de Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
La descarga del SDK de Project 2013 incluye el complemento **Project OM test** Sample que muestra cómo obtener el GUID de una tarea, un recurso y una vista, cómo obtener propiedades del proyecto activo y cómo establecer una tarea, un recurso o un controlador de eventos de vista de selección que ha cambiado. Al extraer e instalar el SDK y los ejemplos en el archivo Project2013SDK. msi, vea el `\Samples\Apps\Copy_to_AppSource_FileShare` subdirectorio y el `\Samples\Apps\Copy_to_AppManifests_FileShare` subdirectorio. El ejemplo archivo jsomcall. html usa funciones de JavaScript en el archivo Office. js y el archivo Project-15. js, que se incluyen en la descarga. Puede usar los archivos de depuración correspondientes (office.debug.js y project-15.debug.js) para examinar las funciones. 
  
El complemento de ejemplo **HelloProject_OData** para Project Professional 2013 se desarrolló con Visual Studio 2012. El complemento usa una consulta REST del servicio **ProjectData** para obtener datos de informes para el costo del proyecto y otra información y, a continuación, compara el proyecto actual con los valores medios de todos los proyectos de Project Web App. 
  
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Complementos de panel de tareas para Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Conexión de un complemento de panel de tareas de Project a PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Descarga del SDK de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Complementos de Office y SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Complementos de Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

