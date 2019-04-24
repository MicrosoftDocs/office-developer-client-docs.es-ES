---
title: Desarrollar con Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Puede incrementar considerablemente las funciones de los formularios de InfoPath ampliándolos con código administrado desarrollado en Visual Studio 2012. Después, puede publicar los formularios con código en las bibliotecas de formularios de SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300290"
---
# <a name="develop-with-visual-studio"></a>Desarrollar con Visual Studio

Puede incrementar considerablemente las funciones de los formularios de InfoPath ampliándolos con código administrado desarrollado en Visual Studio 2012. Después, puede publicar los formularios con código en las bibliotecas de formularios de SharePoint Server 2013.
  
Puede empezar a programar e implementar los formularios de InfoPath con código administrado en tres pasos de alto nivel:
  
1. Instale Visual Studio 2012 con el complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807). 
    
2. Configure el lenguaje de programación y, después, escriba y depure código en el editor de código de Visual Studio 2012.
    
3. Cuando termine de diseñar el formulario y desarrollar el código, podrá publicar la plantilla de formulario en SharePoint Server 2013.
    
Aquí tiene algunos motivos para considerar crear formularios compatibles con SharePoint Server 2013:
  
- Los formularios implementados en SharePoint Server 2013 con InfoPath Forms Services pueden rellenarse en un explorador. De este modo, los usuarios que no tengan instalado InfoPath pueden abrir y usar los formularios.
    
- Solo tiene que diseñar una versión del formulario. Los formularios compatibles con Microsoft SharePoint Server también son compatibles con InfoPath Filler, pero los formularios que solo son compatibles con InfoPath Filler no se pueden abrir en un explorador.
    
Existen dos maneras de publicar formularios en SharePoint: soluciones de espacio aislado de SharePoint y soluciones implementadas por el administrador. Para más información sobre estos métodos de publicación y sugerencias sobre cuál de los dos es mejor para su escenario, vea [Publicar formularios con código](publishing-forms-with-code.md). Vea soluciones de ejemplo de soluciones de espacio aislado en [Soluciones de espacio aislado de ejemplo](sample-sandboxed-solutions.md).
  
## <a name="developing-with-visual-studio"></a>Desarrollar con Visual Studio

Una vez instalados Visual Studio 2012 y el complemento Microsoft Visual Studio Tools for Applications 2012, está listo para empezar a desarrollar soluciones de código administrado de InfoPath.
  
### <a name="choosing-a-programming-language"></a>Seleccionar el lenguaje de programación

InfoPath proporciona las opciones para programar con cuatro versiones del modelo de objetos de InfoPath en dos lenguajes: Visual Basic y C#. Las cuatro versiones del modelo de objetos son compatibles con InfoPath 2013, InfoPath, Office InfoPath 2007 y Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>Para especificar el lenguaje de programación y el modelo de objeto

1. Con un proyecto de plantilla de formulario abierto en el diseñador de InfoPath, haga clic en **Lenguaje** en la pestaña **Programador**. 
    
2. En la categoría **Programación** del cuadro de diálogo **Opciones de formulario**, seleccione el lenguaje con el que quiere trabajar en la lista desplegable **Lenguaje del código de la plantilla del formulario**. Después, seleccione la versión del modelo de objetos en la lista desplegable **Versión de destino**. La opción **Versión de destino** que solo es compatible con InfoPath 2013 no tiene un año de versión siguiendo al nombre **InfoPath**. 
    
    > [!NOTE]
    > [!NOTA] No todos los tipos de plantillas de formulario admiten código. Por ejemplo, los tipos **Lista de SharePoint** y **Elementos de plantillas** no admiten código de formulario. Si diseña un tipo de plantilla de formulario que no admite código, la pestaña **Desarrollador** no está disponible. Por otro lado, solo algunos tipos de plantillas de formulario admiten las cuatro versiones del modelo de objetos. Por ejemplo, el tipo de plantilla **Formulario en blanco (InfoPath Filler)** admite las cuatro versiones del modelo de objetos (y crea plantillas de formularios compatibles solo con InfoPath Filler en esas versiones), pero la plantilla **Formulario en blanco** admite solo InfoPath 2013 y InfoPath (y crea plantillas de formulario compatibles con InfoPath Filler y el explorador). 
  
    Puede establecer un lenguaje de programación predeterminado para que el diseñador de formularios de InfoPath se inicie siempre con el lenguaje y la versión del modelo de objeto que elija.
    
### <a name="to-set-the-default-programming-language"></a>Para establecer el lenguaje de programación predeterminado

1. Haga clic en la pestaña **Archivo** y, a continuación en, **Opciones**.
    
2. En la sección **General** del cuadro de diálogo **Opciones de InfoPath**, haga clic en **Más opciones**.
    
3. En la pestaña **Diseño** del cuadro de diálogo **Opciones**, seleccione el lenguaje de programación predeterminado en la sección **Valores predeterminados de programación**. 
    
### <a name="writing-code"></a>Escribir código

Ahora puede empezar a desarrollar con InfoPath 2013 y Visual Studio 2012. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Para iniciar el editor de código de Visual Studio

1. Abra una plantilla de formulario en el diseñador de InfoPath.
    
2. Haga clic en **Editor de código** en la pestaña **Programador**. 
    
> [!TIP]
> [!SUGERENCIA] También puede iniciar el editor de código y agregar automáticamente controladores de eventos de formulario y control con los comandos de la pestaña **Desarrollador**, los menús contextuales y otros métodos de interfaz de usuario. Para obtener más información, vea [Agregar un controlador de eventos](how-to-add-an-event-handler.md) .
  

