---
title: Usar los miembros del modelo de objetos de SharePoint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Para poder programar con miembros del modelo de objetos de SharePoint a partir de código que se ejecuta en una plantilla de formulario de InfoPath, debe hacer referencia al ensamblado Microsoft.SharePoint.dll en el proyecto de Visual Studio 2012 para el formulario. Para hacerlo, debe tener acceso al sistema de archivos de una copia con licencia de Microsoft SharePoint Server 2010 o de un servidor que ejecute Microsoft SharePoint Foundation 2010 para poder obtener una copia del ensamblado Microsoft.SharePoint.dll.
ms.openlocfilehash: e29725450a6a1bdcba99215e337493f8686491e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303594"
---
# <a name="use-sharepoint-object-model-members"></a>Usar los miembros del modelo de objetos de SharePoint

Para poder programar con miembros del modelo de objetos de SharePoint a partir de código que se ejecuta en una plantilla de formulario de InfoPath, debe hacer referencia al ensamblado Microsoft.SharePoint.dll en el proyecto de Visual Studio 2012 para el formulario. Para hacerlo, debe tener acceso al sistema de archivos de una copia con licencia de Microsoft SharePoint Server 2010 o de un servidor que ejecute Microsoft SharePoint Foundation 2010 para poder obtener una copia del ensamblado Microsoft.SharePoint.dll. 
  
Además, la plantilla de formulario debe estar implementada en el servidor como una solución aprobada por el administrador o de espacio aislado. Para obtener más información sobre estas opciones de implementación, vea [Publicar formularios con código](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Adición del ensamblado Microsoft.SharePoint y referencia a él desde una plantilla de formulario de InfoPath

> [!IMPORTANT]
> [!IMPORTANTE] Para evitar un conflicto con el modo en que el sistema de proyectos de InfoPath administra los archivos que se agregan al archivo de plantilla de formulario, no copie ensamblados a los que desee hacer referencia en la carpeta de nivel superior de un proyecto de plantilla de formulario. De manera predeterminada, será una ruta con el formato siguiente: < *unidad*  >:\Usuarios\  *nombreDeUsuario*  \Documentos\InfoPath Projects\  *nombreDeProyecto* > Si desea mover ensamblados a los que se hace referencia a una ubicación dentro de la carpeta de proyecto, debe crear una subcarpeta en la carpeta de proyecto  *nombreDeProyecto*  principal y copiar los ensamblados y hacer referencia a ellos desde dicha subcarpeta. Sin embargo, tenga en cuenta que no es necesario crear una subcarpeta para los ensamblados a los que se hace referencia. Siempre que el ensamblado al que se haga referencia no esté ubicado dentro de la carpeta de nivel superior del proyecto, el sistema de proyecto de InfoPath lo copiará en el archivo de plantilla de formulario (.xsn) cuando el proyecto se compile y publique. 
  
Microsoft.SharePoint.Server.dll se instala de manera predeterminada en C:\Archivos de programa\Archivos comunes\Microsoft Shared\Web Server\Extensions\14\ISAPI en el sistema de archivos de SharePoint Server 2010 o en un servidor que ejecute SharePoint Foundation 2010.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Para hacer referencia al ensamblado Microsoft.SharePoint desde el proyecto de código de un formulario de InfoPath

1. Copie el ensamblado Microsoft.SharePoint.Server.dll del servidor a una carpeta local, u obtenga acceso al ensamblado desde una carpeta compartida.
    
2. Abra el proyecto de plantilla de formulario en Visual Studio 2012.
    
3. En el menú **Proyecto**, haga clic en **Agregar referencia**.
    
4. Haga clic en la pestaña **Examinar**, busque y especifique el ensamblado y, a continuación, haga clic en **Aceptar** para agregar la referencia. 
    
Ya puede escribir el código en los miembros del modelo de objetos de SharePoint desde el código de formulario. Para facilitar la referencia a miembros del espacio de nombres de Microsoft.SharePoint, agregue  `using Microsoft.SharePoint;` o  `Imports Microsoft.SharePoint` a las directivas al inicio del archivo de código. Para obtener un ejemplo que muestre cómo usar miembros del modelo de objetos de SharePoint en un formulario de InfoPath, vea el ejemplo 2 sobre administración de proveedores en una lista de SharePoint en [Soluciones de espacio aislado de ejemplo](sample-sandboxed-solutions.md).

