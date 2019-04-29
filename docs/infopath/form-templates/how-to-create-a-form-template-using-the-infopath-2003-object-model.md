---
title: Crear una plantilla de formulario con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2007, creating InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: Los procedimientos de este tema describen cómo crear una plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003.
ms.openlocfilehash: 35a9fcfbb0d93a19e013bde6980bc94af3bb5dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418186"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a><span data-ttu-id="de84a-104">Crear una plantilla de formulario con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="de84a-104">Create a Form Template Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="de84a-105">Los procedimientos de este tema describen cómo crear una plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="de84a-105">The procedures in this topic describe how to create a form template that works with the InfoPath 2003-compatible object model.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="de84a-p101">[!IMPORTANTE] Además de los procedimientos siguientes, también debe hacer clic en la pestaña **Archivo**, hacer clic en **Guardar como** y seleccionar **Formulario de plantilla de InfoPath 2003** en el cuadro **Guardar como tipo** para guardar la plantilla en el formato de archivo compatible con InfoPath 2003. Asimismo, para abrir plantillas de formulario compatibles con InfoPath 2003 creadas con InfoPath, todos los usuarios de InfoPath 2003 deben tener .NET Framework 2.0 (o una versión posterior) instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="de84a-p101">In addition to the procedures below, you must also click the **File** tab, click **Save As**, and then select **InfoPath 2003 Form Template** in the **Save as type** box to save the form template to the InfoPath 2003-compatible file format. Also, to open InfoPath 2003-compatible form templates created with InfoPath, all InfoPath 2003 users must have the .NET Framework 2.0 or later installed on their computers.</span></span> 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a><span data-ttu-id="de84a-108">Para crear una plantilla de formulario compatible con InfoPath 2003 en InfoPath con Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="de84a-108">To create an InfoPath 2003-compatible form template in InfoPath with Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="de84a-109">Inicie InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="de84a-109">Start the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="de84a-110">Haga clic en la pestaña **Archivo** y, a continuación, haga clic en **Opciones de formulario**.</span><span class="sxs-lookup"><span data-stu-id="de84a-110">Click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="de84a-111">En la categoría **Compatibilidad**, seleccione **Formulario de editor de InfoPath 2003**.</span><span class="sxs-lookup"><span data-stu-id="de84a-111">In the **Compatibility** category, select **InfoPath 2003 Editor Form**.</span></span>
    
4. <span data-ttu-id="de84a-112">En la categoría **Programación**, seleccione **C# (compatible con InfoPath 2003)** o **Visual Basic (compatible con InfoPath 2003)** en la lista desplegable **Lenguaje del código de la plantilla de formulario**.</span><span class="sxs-lookup"><span data-stu-id="de84a-112">In the **Programming** category, select either **C# (InfoPath 2003 Compatible)** or **Visual Basic (InfoPath 2003 Compatible)** from the **Form template code language** drop-down list.</span></span> 
    
5. <span data-ttu-id="de84a-113">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="de84a-113">Click **OK**.</span></span>
    
6. <span data-ttu-id="de84a-114">Diseñe la plantilla de formulario y, a continuación, agregue controladores de eventos en Visual Studio 2012, tal y como se describe en [Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="de84a-114">Design your form template, and then add event handlers in Visual Studio 2012, as described in [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de84a-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="de84a-115">See also</span></span>



[<span data-ttu-id="de84a-116">Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="de84a-116">Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model</span></span>](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)
  
[<span data-ttu-id="de84a-117">Crear plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="de84a-117">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>](creating-form-templates-using-the-infopath-2003-object-model.md)

