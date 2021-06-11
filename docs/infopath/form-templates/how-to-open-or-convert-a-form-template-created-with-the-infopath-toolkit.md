---
title: Abrir o convertir una plantilla de formulario creada con el objeto InfoPath Toolkit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- converting form templates [infopath 2007],InfoPath Toolkit, opening form templates from,form templates [InfoPath 2007], opening,InfoPath 2007, converting InfoPath Toolkit form templates,opening form templates [InfoPath 2007],form templates [InfoPath 2007], converting,script [InfoPath 2007], converting to managed code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Si creó una plantilla de código administrado en InfoPath 2003 usando el kit de herramientas de InfoPath 2003 para Visual Studio y desea mantener la compatibilidad con InfoPath 2003, puede seguir trabajando y desarrollando el proyecto abriéndolo en Microsoft InfoPath y Visual Studio 2012.
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428588"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Abrir o convertir una plantilla de formulario creada con el objeto InfoPath Toolkit

Si creó una plantilla de código administrado en InfoPath 2003 usando el kit de herramientas de InfoPath 2003 para Visual Studio y desea mantener la compatibilidad con InfoPath 2003, puede seguir trabajando y desarrollando el proyecto abriéndolo en Microsoft InfoPath y Visual Studio 2012.
  
Otra opción es migrar y actualizar el código del proyecto de InfoPath 2003 para usar el nuevo modelo de objetos .NET proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . Cuando lo haga, tendrá que volver a escribir todo el código para usar los miembros del espacio de nombres **Microsoft.Office.InfoPath**, pero todo el código del proyecto anterior se retiene y rodea de instrucciones **#if InfoPathManagedObjectModel** y **#endif** (C#) o **#If InfoPathManagedObject Model** y **#End If** (Visual Basic) como referencia. 
  
En el procedimiento siguiente se describe cómo abrir una plantilla de formulario mediante un código administrado, creada con el kit de herramientas de InfoPath y mantener la compatibilidad con InfoPath 2003, o migrar y actualizar al nuevo modelo de objetos de InfoPath. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Abrir una plantilla de formulario con código administrado creada con el kit de herramientas de InfoPath y mantener la compatibilidad con InfoPath 2003 usando Visual Studio Tools for Applications

1. Abra el Diseñador de InfoPath y haga clic en **Abrir** en la ficha **Archivo**. 
    
2. En el cuadro de diálogo **Abrir en modo Diseño**, desplácese hasta la carpeta de proyecto en la que está guardado el proyecto de plantilla de formulario del kit de herramientas de InfoPath. 
    
    De manera predeterminada, será una carpeta en  `C:\Users\` *nombreUsuario*  `\Documents\Visual Studio Projects` en el equipo en el que se creó el proyecto. O bien, se puede mover la carpeta a la ubicación en la que InfoPath almacena los proyectos de Visual Studio 2012, que de manera predeterminada es  `C:\Users\` *nombreUsuario*  `\Documents\InfoPath Projects`.
    
3. Haga clic en el archivo con el nombre manifest.xsf y, después, haga clic en **Abrir**.
    
4. En la ficha **Programador**, haga clic en **Editor de código**.
    
5. Se mostrará el mensaje "Debe guardar esta plantilla de formulario para poder agregar código de Visual Basic o C# a la misma". Haga clic en **Aceptar** para continuar. 
    
6. Desplácese hasta la ubicación en la que desee guardar el archivo, dé un nombre al archivo y haga clic en **Guardar**.
    
7. Se mostrará el mensaje "Este código se creó con uno de los kits de herramientas de InfoPath 2003 para Microsoft Visual Studio. InfoPath debe migrar el proyecto del kit de herramientas a un nuevo formato". Haga clic en **Aceptar** para continuar. 
    
8. Seleccione el archivo de la solución (.sln) de Visual Studio para el proyecto y haga clic en **Abrir**.
    
9. Se muestra el mensaje "El proyecto se ha migrado" cuando finaliza correctamente el proceso. Haga clic en **Aceptar** para continuar. 
    
10. Se muestra el mensaje "El código de este formulario utiliza el modelo de objetos de InfoPath 2003" con la pregunta "¿Desea actualizar el código para utilizar el modelo de objetos de Microsoft Office InfoPath?" Haga clic en **No** para mantener la compatibilidad con InfoPath 2003 y continúe trabajando con el modelo de objetos proporcionado por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
    
    Para obtener información sobre cómo trabajar con plantillas de formulario compatibles con InfoPath 2003, vea [Programar plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Abrir una plantilla de formulario con código administrado creada con el kit de herramientas de InfoPath y actualizarla para utilizar el nuevo modelo de objetos de InfoPath usando Visual Studio Tools for Applications

1. Abra el Diseñador de InfoPath y haga clic en **Abrir** en la ficha **Archivo**. 
    
2. En **Abrir una plantilla de formulario**, haga clic en **En mi PC**.
    
3. En el cuadro de diálogo **Abrir en modo Diseño**, desplácese hasta la carpeta de proyecto en la que está guardado el proyecto de plantilla de formulario del kit de herramientas de InfoPath. 
    
    De manera predeterminada, será una carpeta en  `C:\Users\` *nombreUsuario*  `\Documents\Visual Studio Projects` en el equipo en el que se creó el proyecto. Otra opción es mover la carpeta a la ubicación en la que InfoPath almacena los proyectos de Visual Studio 2012, que de manera predeterminada es  `C:\Users\` *nombreUsuario*  `\Documents\InfoPath Projects`.
    
4. Haga clic en el archivo con el nombre manifest.xsf y haga clic en **Abrir**.
    
5. En la ficha **Programador**, haga clic en **Editor de código**.
    
6. Se mostrará el mensaje "Debe guardar esta plantilla de formulario para poder agregar código de Visual Basic o C# a la misma". Haga clic en **Aceptar** para continuar. 
    
7. Desplácese hasta la ubicación en la que desee guardar el archivo, dé un nombre al archivo y haga clic en **Guardar**.
    
8. Se mostrará el mensaje "Este código se creó con uno de los kits de herramientas de InfoPath 2003 para Microsoft Visual Studio. InfoPath debe migrar el proyecto del kit de herramientas a un nuevo formato". Haga clic en **Aceptar** para continuar. 
    
9. Seleccione el archivo de la solución (.sln) de Visual Studio para el proyecto y haga clic en **Abrir**.
    
10. Se muestra el mensaje "El proyecto se ha migrado" cuando finaliza correctamente el proceso. Haga clic en **Aceptar** para continuar. 
    
11. Se muestra el mensaje "El código de este formulario utiliza el modelo de objetos de InfoPath 2003" con la pregunta "¿Desea actualizar el código para utilizar el modelo de objetos de Microsoft Office InfoPath?" Haga clic en **Sí** para actualizar la plantilla de formulario para usar el nuevo modelo de objetos de código administrado proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
    
    El código del formulario se abre en el editor de código de Visual Studio 2012 con todo el código del proyecto previo rodeado de instrucciones **#if** **InfoPathManagedObjectModel** y **#endif** (C#) o **#If InfoPathManagedObjectModel** y **#End If** (Visual Basic) como referencia. Tendrá que volver a escribir todo el código para usar los miembros del espacio de nombres **Microsoft.Office.InfoPath**. 
    
    Para obtener información sobre cómo trabajar con plantillas de formulario con código administrado de InfoPath, vea [Desarrollo de plantillas de formulario de InfoPath con código](developing-infopath-form-templates-with-code.md).
    

