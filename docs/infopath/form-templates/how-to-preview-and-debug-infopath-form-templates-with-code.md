---
title: Obtener una vista previa y depurar de plantillas de formulario de InfoPath con código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- previewing form templates [infopath 2007],debugging form templates [InfoPath 2007],form templates [InfoPath 2007], previewing,debugging [InfoPath 2007], managed-code form templates,form templates [InfoPath 2007], debugging,InfoPath 2007, debugging form templates,InfoPath 2007, previewing form templates
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath con Visual Studio 2012 permite la depuración ejecutando el código del formulario en modo de vista previa. Cuando comienza a depurar el código, el proyecto se compila e InfoPath muestra el formulario en la ventana de vista previa. Cuando se encuentra una línea de código en la que se ha establecido un punto de interrupción, el foco se desplaza al editor de código. Si se continúa después del punto de interrupción, el foco vuelve a la ventana de vista previa. La depuración se detiene al cerrar la ventana de vista previa.
ms.openlocfilehash: c33a7740d5f5dba1f8443f020007a2942bc0fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815871"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="3675f-108">Obtener una vista previa y depurar de plantillas de formulario de InfoPath con código</span><span class="sxs-lookup"><span data-stu-id="3675f-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="3675f-p102">Microsoft InfoPath con Visual Studio 2012 permite la depuración ejecutando el código del formulario en modo de vista previa. Cuando comienza a depurar el código, el proyecto se compila e InfoPath muestra el formulario en la ventana de vista previa. Cuando se encuentra una línea de código en la que se ha establecido un punto de interrupción, el foco se desplaza al editor de código. Si se continúa después del punto de interrupción, el foco vuelve a la ventana de vista previa. La depuración se detiene al cerrar la ventana de vista previa.</span><span class="sxs-lookup"><span data-stu-id="3675f-p102">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode. When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window. When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor. When you continue past a breakpoint, the focus moves back to the preview window. Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="3675f-114">También puede modificar las opciones de la plantilla de formulario para obtener la vista previa y depurar usando un rol de usuario específico, un archivo de datos de ejemplo o especificando el dominio en el que se publicará el formulario.</span><span class="sxs-lookup"><span data-stu-id="3675f-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3675f-115">[!NOTA] No es posible depurar plantillas de formulario después de implementarlas en tiempo de ejecución en Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="3675f-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="3675f-116">Esto incluye las plantillas de formulario que son compatibles solo con InfoPath, así como las compatibles con InfoPath y el explorador web que usa InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="3675f-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="3675f-117">No obstante, es posible registrar los valores en un campo desde el código en tiempo de ejecución para facilitar la depuración de la lógica empresarial de una plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="3675f-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="3675f-118">Para obtener información acerca de cómo hacerlo, vea [Los valores del registro a un campo para la depuración](how-to-log-values-to-a-field-for-debugging.md).</span><span class="sxs-lookup"><span data-stu-id="3675f-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="3675f-119">Depurar en modo de vista previa</span><span class="sxs-lookup"><span data-stu-id="3675f-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="3675f-120">Depurar un proyecto de InfoPath en modo de vista previa</span><span class="sxs-lookup"><span data-stu-id="3675f-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="3675f-121">Cree o abra un proyecto de plantilla de formulario con código administrado de InfoPath en Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="3675f-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="3675f-122">Establezca uno o más puntos de interrupción en el código del formulario en el editor de código haciendo clic en la barra gris situada a la izquierda de la línea de código en la que desea insertar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="3675f-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="3675f-123">Aparecerá un círculo rojo y la línea de código se resaltará para indicar que, en tiempo de ejecución, se hará una pausa al llegar a este punto en el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="3675f-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="3675f-124">En el menú **Depurar**, haga clic en **Iniciar depuración** (o presione F5).</span><span class="sxs-lookup"><span data-stu-id="3675f-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="3675f-125">El proyecto se compilará y se mostrará el formulario en la ventana de vista previa.</span><span class="sxs-lookup"><span data-stu-id="3675f-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="3675f-126">Interactúe con el formulario hasta que encuentre una línea de código que contenga un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="3675f-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="3675f-127">El foco volverá al editor de código.</span><span class="sxs-lookup"><span data-stu-id="3675f-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="3675f-128">En el menú **Depurar**, haga clic en **Continuar** o bien presione F5.</span><span class="sxs-lookup"><span data-stu-id="3675f-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="3675f-129">Cuando haya finalizado la depuración, cierre la ventana de vista previa, haga clic en **Detener depuración** en el menú **Depurar**.</span><span class="sxs-lookup"><span data-stu-id="3675f-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3675f-130">Para depurar una plantilla de formulario de código administrado de InfoPath cuando se usa a un miembro del modelo de objeto que requiere plena confianza, debe configurar la plantilla de formulario como se describe en la [vista previa y depurar plantillas de formulario que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="3675f-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="3675f-131">Usar un archivo de datos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3675f-131">Using a Sample Data File</span></span>

<span data-ttu-id="3675f-p104">De manera predeterminada, la depuración y la vista previa utilizan el archivo template.xml que se crea junto con el proyecto. Puede crear su propio archivo de datos y especificar si desea utilizarlo al obtener la vista previa o depurar mediante el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="3675f-p104">By default, debugging and previewing uses the template.xml file that is created when a form template is created. You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="3675f-134">Para especificar un archivo de datos de ejemplo para usarlo durante la depuración o la vista previa en Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="3675f-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="3675f-135">Para ver template.xml, abra la plantilla de formulario en el modo de edición.</span><span class="sxs-lookup"><span data-stu-id="3675f-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="3675f-136">Haga clic en la pestaña **Archivo**, haga clic en **Guardar**, haga clic en **Guardar plantilla de formulario como** y haga clic en **Archivos de origen**.</span><span class="sxs-lookup"><span data-stu-id="3675f-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="3675f-137">Guarde los archivos de plantilla de formulario en una carpeta y después abra el archivo template.xml en un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="3675f-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="3675f-138">Cree y guarde un archivo con la misma estructura que template.xml con los datos de ejemplo que desea usar.</span><span class="sxs-lookup"><span data-stu-id="3675f-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="3675f-139">Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**.</span><span class="sxs-lookup"><span data-stu-id="3675f-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="3675f-140">Haga clic en la categoría **Vista previa** del cuadro de diálogo **Opciones de formulario** y a continuación, bajo **Datos de ejemplo**, especifique el archivo de datos de ejemplo que creó en el cuadro **Ubicación de archivo**.</span><span class="sxs-lookup"><span data-stu-id="3675f-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="3675f-141">Especificar un rol de usuario para utilizarlo durante la depuración o la vista previa</span><span class="sxs-lookup"><span data-stu-id="3675f-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="3675f-p105">Si el formulario con el que está trabajando tiene definidos roles de usuario, puede especificar uno de ellos para utilizarlo durante la depuración o la vista previa. Para obtener información sobre cómo definir roles de usuario, busque "rol de usuario" en la Ayuda de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3675f-p105">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form. For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="3675f-p106">[!NOTA] La opción de especificar un rol de usuario no está disponible si la configuración de compatibilidad de la plantilla de formulario está establecida en **Formulario de explorador web**. Los roles de usuario no se admiten en las plantillas de formulario que se abren en el explorador desde InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="3675f-p106">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**. User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="3675f-146">Para especificar un rol de usuario para utilizarlo durante la depuración o la vista previa</span><span class="sxs-lookup"><span data-stu-id="3675f-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="3675f-147">Si está trabajando en Visual Studio 2012, cambie a InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="3675f-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="3675f-148">Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**.</span><span class="sxs-lookup"><span data-stu-id="3675f-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="3675f-149">Haga clic en la categoría **Vista previa** del cuadro de diálogo **Opciones de formulario** y especifique el rol de usuario en el cuadro desplegable **Vista previa como**.</span><span class="sxs-lookup"><span data-stu-id="3675f-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="3675f-150">Especificar un dominio para utilizarlo durante la depuración o la vista previa</span><span class="sxs-lookup"><span data-stu-id="3675f-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="3675f-p107">Puede tener una vista previa de un formulario según se publicó en un dominio específico. Esta configuración se aplicará únicamente si el nivel de seguridad de la plantilla de formulario está establecido en **Dominio**.</span><span class="sxs-lookup"><span data-stu-id="3675f-p107">You can preview a form as if it was published to a specific domain. This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="3675f-153">Para especificar un dominio para utilizarlo durante la depuración o la vista previa</span><span class="sxs-lookup"><span data-stu-id="3675f-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="3675f-154">Si está trabajando en Visual Studio 2012, cambie a InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="3675f-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="3675f-155">Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**.</span><span class="sxs-lookup"><span data-stu-id="3675f-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="3675f-156">Haga clic en la categoría **Vista previa** del cuadro de diálogo **Opciones de formulario** y especifique el dominio que usará durante la vista previa y la depuración en el cuadro **Dominio**.</span><span class="sxs-lookup"><span data-stu-id="3675f-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="3675f-157">Haga clic en la categoría **Seguridad y confianza** del cuadro de diálogo **Opciones de formulario**, desactive la casilla **Determinar automáticamente el nivel de seguridad** y después haga clic en **Dominio**.</span><span class="sxs-lookup"><span data-stu-id="3675f-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

