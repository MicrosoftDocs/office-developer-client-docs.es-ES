---
title: 'Tutorial: Crear y depurar una plantilla de formulario básica con el modelo de objetos de InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], walkthroughs,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: En este tema se proporciona un tutorial sobre la creación de una plantilla de formulario de código administrado de InfoPath básica que funciona con el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414343"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="8ba55-104">Tutorial: Crear y depurar una plantilla de formulario básica con el modelo de objetos de InfoPath</span><span class="sxs-lookup"><span data-stu-id="8ba55-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="8ba55-105">En este tema se proporciona un tutorial sobre la creación de una plantilla de formulario con código administrado de InfoPath básica que funciona con el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba55-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="8ba55-106">Hola a todos</span><span class="sxs-lookup"><span data-stu-id="8ba55-106">Hello World</span></span>

<span data-ttu-id="8ba55-107">En el siguiente ejemplo, aprenderá a mostrar un cuadro de diálogo de alerta simple mediante el método [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) del modelo de objetos compatible con InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8ba55-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="8ba55-108">Crear una plantilla de formulario de InfoPath que funciona con el modelo de objetos compatible con InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="8ba55-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="8ba55-109">Cree una nueva plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003, tal como se describe en Crear una plantilla de formulario mediante el modelo de objetos de [InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="8ba55-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="8ba55-110">Asigne al proyecto de plantilla de formulario el nombre HelloWorld y guárdelo.</span><span class="sxs-lookup"><span data-stu-id="8ba55-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="8ba55-p101">El sistema de proyectos crea el código y los archivos del proyecto y, a continuación, abre una plantilla de formulario en blanco en el modo de diseño de InfoPath. Ya está listo para añadir controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="8ba55-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="8ba55-113">Agregar un botón con un controlador de eventos OnClick</span><span class="sxs-lookup"><span data-stu-id="8ba55-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="8ba55-114">En la sección **Controles** de la ficha **Inicio**, haga clic en el control **Botón** para insertarlo en la vista.</span><span class="sxs-lookup"><span data-stu-id="8ba55-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="8ba55-115">Haga clic con el botón secundario del mouse en el control y a continuación haga clic en **Propiedades del botón**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="8ba55-116">Cambie la **etiqueta a** Alerta.</span><span class="sxs-lookup"><span data-stu-id="8ba55-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="8ba55-117">Cambie el **identificador a** AlertID.</span><span class="sxs-lookup"><span data-stu-id="8ba55-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="8ba55-118">Haga clic en **Editar código del formulario**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="8ba55-119">Se crea un esqueleto del controlador de eventos para el evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) y el foco se mueve al editor de código Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="8ba55-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="8ba55-120">Para obtener más información sobre cómo trabajar con controladores de eventos, vea Agregar un controlador de eventos mediante el modelo de objetos de [InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="8ba55-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="8ba55-121">Ya está todo preparado para agregar el código de formulario al controlador de eventos del botón.</span><span class="sxs-lookup"><span data-stu-id="8ba55-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="8ba55-122">Agregar código de formulario al controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="8ba55-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="8ba55-123">En el controlador de eventos **OnClick**, escriba el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="8ba55-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="8ba55-p103">Observe que aparece una lista desplegable de Microsoft IntelliSense cada vez que se escribe un punto en la línea de código. La función completa del controlador de eventos debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="8ba55-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > <span data-ttu-id="8ba55-126">Como alternativa al método **Alert**, puede utilizar el método **MessageBox.Show** del espacio de nombres **System.Windows.Forms** para mostrar un cuadro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8ba55-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="8ba55-127">Para ello, debe agregar una referencia al ensamblado System.Windows.Forms, agregar o a las directivas al principio del archivo de código y, a continuación, escribir una línea de código como la  `using System.Windows.Forms;`  `Imports System.Windows.Forms` siguiente:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="8ba55-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="8ba55-128">Cambie a la ventana de modo de diseño de InfoPath y haga clic en el botón **Vista previa** de la ficha **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="8ba55-129">En la ventana **Vista previa**, haga clic en el botón **Aviso**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="8ba55-130">Aparecerá un cuadro de mensaje con el texto "Hello World".</span><span class="sxs-lookup"><span data-stu-id="8ba55-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="8ba55-131">El procedimiento siguiente muestra cómo agregar puntos de interrupción para depurar el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="8ba55-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="8ba55-132">Depurar el código del formulario</span><span class="sxs-lookup"><span data-stu-id="8ba55-132">Debug form code</span></span>

1. <span data-ttu-id="8ba55-133">En el editor de código, haga clic en la barra gris que se encuentra a la izquierda de esta línea:</span><span class="sxs-lookup"><span data-stu-id="8ba55-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="8ba55-134">Aparecerá un círculo rojo y la línea de código se resaltará para indicar que se hará una pausa en el tiempo de ejecución al llegar a este punto de interrupción en el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="8ba55-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="8ba55-135">En el menú **Depurar**, haga clic en **Iniciar depuración** (o presione F5).</span><span class="sxs-lookup"><span data-stu-id="8ba55-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="8ba55-136">En la ventana **Vista previa** de InfoPath, haga clic en el botón **Aviso**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="8ba55-137">El foco se desplazará al editor de código y se resaltará la línea en la que se encuentra el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8ba55-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="8ba55-138">En el menú **Depurar**, haga clic en **Paso a paso por procedimientos** (o presione Mayús+F8) para continuar depurando el código paso a paso.</span><span class="sxs-lookup"><span data-stu-id="8ba55-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="8ba55-139">Se **ejecuta** el código del método Alert y "Hello World!".</span><span class="sxs-lookup"><span data-stu-id="8ba55-139">The **Alert** method code is executed, and the "Hello World!"</span></span> <span data-ttu-id="8ba55-140">se muestra en la ventana vista previa **de** InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8ba55-140">alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="8ba55-141">Obtener el nombre del usuario actual</span><span class="sxs-lookup"><span data-stu-id="8ba55-141">Getting the Current User's Name</span></span>

<span data-ttu-id="8ba55-p106">Puede utilizar las clases de .NET Framework para obtener acceso a funciones de las que no se puede disponer con facilidad en las secuencias de comandos. En este ejemplo, aprenderá cómo utilizar las clases de .NET Framework para recuperar el nombre del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8ba55-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="8ba55-144">Agregar un controlador de eventos OnLoad</span><span class="sxs-lookup"><span data-stu-id="8ba55-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="8ba55-145">Abra el proyecto HelloWorld de InfoPath que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="8ba55-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="8ba55-146">En la ficha **Ver**, haga clic en **Mostrar campos**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="8ba55-147">Haga clic con el botón secundario en el nodo **myFields** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="8ba55-148">En **Nombre**, escriba **empleado** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="8ba55-149">Arrastre el nodo **empleado** hasta la vista.</span><span class="sxs-lookup"><span data-stu-id="8ba55-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="8ba55-150">En la ficha **Programador**, haga clic en **Evento Al cargar (OnLoad)**.</span><span class="sxs-lookup"><span data-stu-id="8ba55-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="8ba55-151">Esto creará un controlador de eventos para el evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) y el foco se moverá al editor de código.</span><span class="sxs-lookup"><span data-stu-id="8ba55-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="8ba55-152">Se puede llamar al código de este controlador de eventos cada vez que se cargue el formulario.</span><span class="sxs-lookup"><span data-stu-id="8ba55-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="8ba55-153">El procedimiento siguiente muestra cómo agregar código de formulario que recupere el nombre del usuario para el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="8ba55-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="8ba55-154">Agregar código de formulario</span><span class="sxs-lookup"><span data-stu-id="8ba55-154">Add form code</span></span>

1. <span data-ttu-id="8ba55-155">En el controlador de eventos **OnLoad**, escriba el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="8ba55-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. <span data-ttu-id="8ba55-156">Compile el formulario y obtenga una vista previa del mismo.</span><span class="sxs-lookup"><span data-stu-id="8ba55-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="8ba55-157">El nombre de usuario debería aparecer ahora en el cuadro de texto Empleado.</span><span class="sxs-lookup"><span data-stu-id="8ba55-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="8ba55-158">Para obtener información acerca de cómo implementar una plantilla de formulario con código administrado, vea Implementar plantillas de formulario [de InfoPath con código.](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="8ba55-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="8ba55-159">Para obtener información sobre el modelo de objetos de InfoPath y las tareas de programación comunes en plantillas de formulario con código administrado que funcionan con el modelo de objetos compatible con InfoPath 2003, vea Descripción del modelo de objetos de [InfoPath 2003](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="8ba55-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ba55-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ba55-160">See also</span></span>

- [<span data-ttu-id="8ba55-161">Utilizar código de limpieza e inicialización mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="8ba55-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="8ba55-162">Modelos de objetos compatibles con InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="8ba55-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="8ba55-163">Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="8ba55-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

