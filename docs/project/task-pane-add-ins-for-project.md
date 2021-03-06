---
title: Complementos del Panel de tareas de Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 y Project Profesional 2013 admiten el panel de tareas Office complementos. Puede usar complementos de panel de tareas para integrar datos de proyectos, tareas, recursos y vistas en un proyecto con otras aplicaciones cliente de Office 2013, aplicaciones de SharePoint, elementos web, otras páginas web y datos externos.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330019"
---
# <a name="task-pane-add-ins-for-project"></a>Complementos del Panel de tareas de Project

Project Standard 2013 y Project Profesional 2013 admiten el panel de tareas Office complementos. Puede usar complementos de panel de tareas para integrar datos de proyectos, tareas, recursos y vistas en un proyecto con otras aplicaciones cliente de Office 2013, aplicaciones de SharePoint, elementos web, otras páginas web y datos externos.
  
Office Los complementos son un modelo de extensibilidad que se admite en varias Office cliente de 2013. La plataforma de complementos completa incluye tipos de complementos contextuales, de contenido y de panel de tareas. Outlook 2013 admite complementos de correo, que pueden mostrar una página web dentro de un mensaje de correo electrónico o elemento de cita de calendario relacionado con el contenido del elemento. Word 2013 y Excel 2013 admiten complementos de contenido, que pueden mostrar una página web como contenido incrustado en un documento. Word 2013, Excel 2013 y Project Profesional 2013 admiten complementos de panel de tareas, que pueden mostrar una página web en un panel de tareas donde el contenido está relacionado con información contextual dentro del proyecto.
  
Por ejemplo, un Project complemento puede resumir los datos del proyecto activo y mostrar datos adicionales sobre una tarea o recurso seleccionado. Los datos relacionados en el complemento pueden provienen de un origen externo, como una lista de SharePoint, tablas de informes en la base de datos de Project Server, un servicio web u otra aplicación de empresa. Un complemento de panel de tareas se puede desarrollar con HTML 5, JavaScript, JQuery y otras bibliotecas de JavaScript. Un complemento de panel de tareas no admite directamente ActiveX, Silverlight o componentes flash. Aunque un complemento Office podría usar un elemento **IFrame** para tener acceso a una aplicación web del lado servidor que usa ASP.NET y la biblioteca de .NET Framework 4.5, ese tipo de solución no se recomienda ni admite. El complemento se puede desarrollar para guardar datos localmente o escribir datos en una ubicación externa. 
  
> [!NOTE]
> Los complementos Project panel de tareas pueden obtener acceso a los datos Project Online mediante la autenticación de OAuth. Con Project Profesional 2013, puede desarrollar complementos de panel de tareas que accedan tanto a instalaciones locales de Project Server 2013 como locales o en línea SharePoint 2013. Por ejemplo, vea [Connecting a Project Task Pane add-in to PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) en el blog Project Programmibility. > Project Standard 2013 no admite la integración directa con los datos de Project Server ni las SharePoint de tareas sincronizadas con Project Server. 
  
Para obtener más información acerca de los complementos para Office 2013, vea Office [y SharePoint Complementos](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Desarrollo de complementos de panel de tareas

La documentación para desarrolladores Office y SharePoint complementos incluye artículos y referencias completas. Para obtener una introducción al desarrollo de complementos para Project Profesional 2013 y otras aplicaciones cliente de Office 2013, y para la referencia de JavaScript y la referencia de manifiesto XML, vea [Office Add-ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
La descarga del SDK de Project 2013 incluye el complemento de ejemplo de prueba de OM de **Project** que muestra cómo obtener el GUID de una tarea, un recurso y una vista, cómo obtener propiedades del proyecto activo y cómo establecer un controlador de eventos modificado de selección, recurso o tarea. Al extraer e instalar el SDK y los ejemplos en el archivo Project2013SDK.msi, vea el  `\Samples\Apps\Copy_to_AppSource_FileShare` subdirectorio y el  `\Samples\Apps\Copy_to_AppManifests_FileShare` subdirectorio. El ejemplo JSOMCall.html usa funciones de JavaScript en el archivo office.js archivo y project-15.js archivo, que se incluyen en la descarga. Puede usar los archivos de depuración correspondientes (office.debug.js y project-15.debug.js) para examinar las funciones. 
  
El **HelloProject_OData** de ejemplo para Project Profesional 2013 se desarrolló con Visual Studio 2012. El complemento usa una consulta REST del servicio **ProjectData** para obtener datos de informes para el costo del proyecto y otra información y, a continuación, compara el proyecto actual con los valores promedio de todos los proyectos de Project Web App. 
  
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Complementos de panel de tareas para Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Conexión de un Project de panel de tareas a PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Descarga del SDK de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Complementos de Office y SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Complementos de Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

