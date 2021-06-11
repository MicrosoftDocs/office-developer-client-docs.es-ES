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
# <a name="develop-with-visual-studio"></a><span data-ttu-id="712cb-104">Desarrollar con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="712cb-104">Develop with Visual Studio</span></span>

<span data-ttu-id="712cb-p102">Puede incrementar considerablemente las funciones de los formularios de InfoPath ampliándolos con código administrado desarrollado en Visual Studio 2012. Después, puede publicar los formularios con código en las bibliotecas de formularios de SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="712cb-p102">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012. You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="712cb-107">Puede empezar a programar e implementar los formularios de InfoPath con código administrado en tres pasos de alto nivel:</span><span class="sxs-lookup"><span data-stu-id="712cb-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="712cb-108">Instale Visual Studio 2012 con el complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807).</span><span class="sxs-lookup"><span data-stu-id="712cb-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="712cb-109">Configure el lenguaje de programación y, después, escriba y depure código en el editor de código de Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="712cb-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="712cb-110">Cuando termine de diseñar el formulario y desarrollar el código, podrá publicar la plantilla de formulario en SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="712cb-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="712cb-111">Aquí tiene algunos motivos para considerar crear formularios compatibles con SharePoint Server 2013:</span><span class="sxs-lookup"><span data-stu-id="712cb-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="712cb-p103">Los formularios implementados en SharePoint Server 2013 con InfoPath Forms Services pueden rellenarse en un explorador. De este modo, los usuarios que no tengan instalado InfoPath pueden abrir y usar los formularios.</span><span class="sxs-lookup"><span data-stu-id="712cb-p103">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser. This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="712cb-p104">Solo tiene que diseñar una versión del formulario. Los formularios compatibles con Microsoft SharePoint Server también son compatibles con InfoPath Filler, pero los formularios que solo son compatibles con InfoPath Filler no se pueden abrir en un explorador.</span><span class="sxs-lookup"><span data-stu-id="712cb-p104">You design only one version of the form. Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="712cb-p105">Existen dos maneras de publicar formularios en SharePoint: soluciones de espacio aislado de SharePoint y soluciones implementadas por el administrador. Para más información sobre estos métodos de publicación y sugerencias sobre cuál de los dos es mejor para su escenario, vea [Publicar formularios con código](publishing-forms-with-code.md). Vea soluciones de ejemplo de soluciones de espacio aislado en [Soluciones de espacio aislado de ejemplo](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="712cb-p105">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions. For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md). For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="712cb-119">Desarrollar con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="712cb-119">Developing with Visual Studio</span></span>

<span data-ttu-id="712cb-120">Una vez instalados Visual Studio 2012 y el complemento Microsoft Visual Studio Tools for Applications 2012, está listo para empezar a desarrollar soluciones de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="712cb-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="712cb-121">Seleccionar el lenguaje de programación</span><span class="sxs-lookup"><span data-stu-id="712cb-121">Choosing a Programming Language</span></span>

<span data-ttu-id="712cb-p106">InfoPath proporciona las opciones para programar con cuatro versiones del modelo de objetos de InfoPath en dos lenguajes: Visual Basic y C#. Las cuatro versiones del modelo de objetos son compatibles con InfoPath 2013, InfoPath, Office InfoPath 2007 y Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="712cb-p106">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#. The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="712cb-124">Para especificar el lenguaje de programación y el modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="712cb-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="712cb-125">Con un proyecto de plantilla de formulario abierto en el diseñador de InfoPath, haga clic en **Lenguaje** en la pestaña **Programador**.</span><span class="sxs-lookup"><span data-stu-id="712cb-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="712cb-p107">En la categoría **Programación** del cuadro de diálogo **Opciones de formulario**, seleccione el lenguaje con el que quiere trabajar en la lista desplegable **Lenguaje del código de la plantilla del formulario**. Después, seleccione la versión del modelo de objetos en la lista desplegable **Versión de destino**. La opción **Versión de destino** que solo es compatible con InfoPath 2013 no tiene un año de versión siguiendo al nombre **InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="712cb-p107">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list. Then, select the version of the object model from the **Target version** drop-down list. The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="712cb-p108">[!NOTA] No todos los tipos de plantillas de formulario admiten código. Por ejemplo, los tipos **Lista de SharePoint** y **Elementos de plantillas** no admiten código de formulario. Si diseña un tipo de plantilla de formulario que no admite código, la pestaña **Desarrollador** no está disponible. Por otro lado, solo algunos tipos de plantillas de formulario admiten las cuatro versiones del modelo de objetos. Por ejemplo, el tipo de plantilla **Formulario en blanco (InfoPath Filler)** admite las cuatro versiones del modelo de objetos (y crea plantillas de formularios compatibles solo con InfoPath Filler en esas versiones), pero la plantilla **Formulario en blanco** admite solo InfoPath 2013 y InfoPath (y crea plantillas de formulario compatibles con InfoPath Filler y el explorador).</span><span class="sxs-lookup"><span data-stu-id="712cb-p108">Not all form template types support code. For example, the **SharePoint List** form template type and **Template Parts** do not support form code. When designing a form template type that does not support code, the **Developer** tab will not be available. Also, only some form template types support all four versions of the object model. For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="712cb-134">Puede establecer un lenguaje de programación predeterminado para que el diseñador de formularios de InfoPath se inicie siempre con el lenguaje y la versión del modelo de objeto que elija.</span><span class="sxs-lookup"><span data-stu-id="712cb-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="712cb-135">Para establecer el lenguaje de programación predeterminado</span><span class="sxs-lookup"><span data-stu-id="712cb-135">To set the default programming language</span></span>

1. <span data-ttu-id="712cb-136">Haga clic en la pestaña **Archivo** y, a continuación en, **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="712cb-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="712cb-137">En la sección **General** del cuadro de diálogo **Opciones de InfoPath**, haga clic en **Más opciones**.</span><span class="sxs-lookup"><span data-stu-id="712cb-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="712cb-138">En la pestaña **Diseño** del cuadro de diálogo **Opciones**, seleccione el lenguaje de programación predeterminado en la sección **Valores predeterminados de programación**.</span><span class="sxs-lookup"><span data-stu-id="712cb-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="712cb-139">Escribir código</span><span class="sxs-lookup"><span data-stu-id="712cb-139">Writing Code</span></span>

<span data-ttu-id="712cb-140">Ahora puede empezar a desarrollar con InfoPath 2013 y Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="712cb-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="712cb-141">Para iniciar el editor de código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="712cb-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="712cb-142">Abra una plantilla de formulario en el diseñador de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="712cb-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="712cb-143">Haga clic en **Editor de código** en la pestaña **Programador**.</span><span class="sxs-lookup"><span data-stu-id="712cb-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="712cb-144">[!SUGERENCIA] También puede iniciar el editor de código y agregar automáticamente controladores de eventos de formulario y control con los comandos de la pestaña **Desarrollador**, los menús contextuales y otros métodos de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="712cb-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="712cb-145">Para obtener más información, vea [Agregar un controlador de eventos](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="712cb-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

