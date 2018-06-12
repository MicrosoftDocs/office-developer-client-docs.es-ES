---
title: Complementos de panel de tareas para Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 y Project Professional 2013 ambos admiten el panel de tareas Office Add-ins. Puede utilizar complementos de panel de tareas para integrar el proyecto, tarea, recurso y ver los datos en un proyecto con otras aplicaciones cliente de Office 2013, las aplicaciones de SharePoint, elementos Web, otras páginas Web y datos externos.
ms.openlocfilehash: 1432f38e9f2c87b7d5d33500d958222b2c15d7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821437"
---
# <a name="task-pane-add-ins-for-project"></a>Complementos de panel de tareas para Project

Project Standard 2013 y Project Professional 2013 ambos admiten el panel de tareas Office Add-ins. Puede utilizar complementos de panel de tareas para integrar el proyecto, tarea, recurso y ver los datos en un proyecto con otras aplicaciones cliente de Office 2013, las aplicaciones de SharePoint, elementos Web, otras páginas Web y datos externos.
  
Complementos de Office es un modelo de extensibilidad que se admite en varias aplicaciones de cliente de Office 2013. La plataforma completa complemento incluye contextual, contenido y tipos de complementos de panel de tareas. Outlook 2013 es compatible con complementos del correo, que pueden mostrar una página Web dentro de un mensaje de correo electrónico o elemento de cita de calendario que está relacionado con contenido en el elemento. 2013 de Word y Excel 2013 admiten complementos contenidos, que pueden mostrar una página Web como contenido incrustado en un documento. Word 2013, Excel 2013 y Project Professional 2013 admiten tarea panel complementos, que pueden mostrar una página Web en un panel de tareas donde el contenido está relacionado con información contextual dentro del proyecto.
  
Por ejemplo, un complemento de Project puede resumir los datos en el proyecto activo y mostrar datos adicionales sobre una tarea o recurso seleccionado. Datos relacionados en el complemento pueden proceder de un origen externo como una lista de SharePoint, informes de tablas en la base de datos de Project Server, un servicio web o en otra aplicación de empresa. Un complemento del panel de tareas se puede desarrollar con 5 de HTML, JavaScript, JQuery y otras bibliotecas de JavaScript. Un complemento del panel de tareas no admite directamente ActiveX, Silverlight o componentes de Flash. Aunque un complemento de Office podría usar un elemento **IFrame** para tener acceso a una aplicación de servidor web que utiliza ASP.NET y la biblioteca de .NET Framework 4.5, ese tipo de solución no se recomienda o compatible. El complemento puede desarrollarse para guardar los datos localmente o escribir datos en una ubicación externa. 
  
> [!NOTE]
> Project Add-ins del panel de tareas puede obtener acceso a datos desde Project Online mediante el uso de la autenticación de OAuth. Con Project Professional 2013, puede desarrollar tareas panel complementos que tienen acceso a las instalaciones locales de Project Server 2013 y local o en línea de SharePoint de 2013. Por ejemplo, vea [Conectar un panel de tareas de proyecto de complemento para PWA](http://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) en el blog de Programmibility del proyecto. > Project Standard 2013 no admite la integración directa con datos de Project Server o listas de tareas de SharePoint que se sincronizan con Project Server. 
  
Para obtener más información sobre complementos para Office 2013, vea [Office y SharePoint Add-ins](http://msdn.microsoft.com/en-us/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Desarrollo de complementos de panel de tareas

La documentación para desarrolladores de Office y SharePoint Add-ins incluye referencias y artículos completa. Para obtener una introducción al desarrollo de complementos para Project Professional 2013 y otras aplicaciones de cliente de Office 2013 y para la referencia de JavaScript y referencia XML de manifiesto, vea [Office Add-ins](http://msdn.microsoft.com/en-us/library/office/apps/jj220060%28v=office.15%29).
  
La descarga del SDK de Project 2013 incluye el complemento de ejemplo de **Project OM Test** que se muestra cómo obtener el GUID de una tarea, recurso y vista, cómo obtener propiedades del proyecto activo y cómo establecer una tarea, recurso, o ver el controlador de eventos de cambio de selección. Al extraer e instalar el SDK y ejemplos en el archivo Project2013SDK.msi, vea el `\Samples\Apps\Copy_to_AppSource_FileShare` subdirectorio y la `\Samples\Apps\Copy_to_AppManifests_FileShare` subdirectorio. En el ejemplo JSOMCall.html usa las funciones de JavaScript en el archivo office.js y el archivo project-15.js, que se incluyen en la descarga. Puede usar los archivos de depuración correspondientes (office.debug.js y project-15.debug.js) para examinar las funciones. 
  
El complemento de ejemplo con **HelloProject_OData** para Project Professional 2013 desarrollado con Visual Studio 2012. El complemento usa una consulta REST del servicio **ProjectData** para obtener informes de datos de costo de proyecto y otra información y, a continuación, compara el proyecto actual con los valores promedio para todos los proyectos en Project Web App. 
  
## <a name="see-also"></a>Ver también
<a name="bk_addresources"> </a>

- [Complementos de tarea panel para Project](http://msdn.microsoft.com/en-us/library/office/apps/fp161143%28v=office.15%29)
    
- [Conectar un complemento en el panel de tareas de proyecto en PWA](http://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Descarga del SDK de Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office y SharePoint Add-ins](http://msdn.microsoft.com/en-us/library/office/fp161507%28v=office.15%29)
    
- [Complementos de Office](http://msdn.microsoft.com/en-us/library/office/apps/jj220060%28v=office.15%29)
    

