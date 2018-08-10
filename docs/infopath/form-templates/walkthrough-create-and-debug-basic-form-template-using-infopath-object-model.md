---
title: 'Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], walkthroughs,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: En este tema se ofrece un tutorial que enseña a crear una plantilla de formulario básica con código administrado de InfoPath, que funciona con el modelo de objetos compatible con InfoPath 2003 suministrado por los miembros del espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust .
ms.openlocfilehash: 3939cfcfdf2a8683fe614c5f49cc8b2719484ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815973"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="9a058-104">Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath</span><span class="sxs-lookup"><span data-stu-id="9a058-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="9a058-105">En este tema se ofrece un tutorial que enseña a crear una plantilla de formulario básica con código administrado de InfoPath, que funciona con el modelo de objetos compatible con InfoPath 2003 suministrado por los miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9a058-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="9a058-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="9a058-106">Hello World</span></span>

<span data-ttu-id="9a058-107">En el ejemplo siguiente, aprenderá cómo mostrar un sencillo cuadro de diálogo de alerta mediante el método [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) del modelo de objetos de InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="9a058-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="9a058-108">Crear una plantilla de formulario de InfoPath que funciona con el modelo de objetos compatible con InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a058-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="9a058-109">Crear una nueva plantilla de formulario que funciona con el modelo de objetos compatible con InfoPath 2003, tal como se describe en [crear una plantilla de formulario mediante el modelo de objetos de InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9a058-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="9a058-110">Asigne al proyecto de plantilla de formulario el nombre HelloWorld y guárdelo.</span><span class="sxs-lookup"><span data-stu-id="9a058-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="9a058-p101">El sistema de proyectos crea el código y los archivos del proyecto y, a continuación, abre una plantilla de formulario en blanco en el modo de diseño de InfoPath. Ya está listo para añadir controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="9a058-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="9a058-113">Agregar un botón con un controlador de eventos OnClick</span><span class="sxs-lookup"><span data-stu-id="9a058-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="9a058-114">En la sección **Controles** de la ficha **Inicio**, haga clic en el control **Botón** para insertarlo en la vista.</span><span class="sxs-lookup"><span data-stu-id="9a058-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="9a058-115">Haga clic con el botón secundario del mouse en el control y a continuación haga clic en **Propiedades del botón**.</span><span class="sxs-lookup"><span data-stu-id="9a058-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="9a058-116">Cambie la **etiqueta** a Alerta.</span><span class="sxs-lookup"><span data-stu-id="9a058-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="9a058-117">Cambie el **Id.** a IdAlerta.</span><span class="sxs-lookup"><span data-stu-id="9a058-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="9a058-118">Haga clic en **Editar código del formulario**.</span><span class="sxs-lookup"><span data-stu-id="9a058-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="9a058-119">Se crea un esqueleto de controlador de eventos para el evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) y el foco se desplaza al editor de código en Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="9a058-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="9a058-120">Para obtener más información sobre cómo trabajar con controladores de eventos, vea [Agregar un controlador de eventos con el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9a058-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="9a058-121">Ya está todo preparado para agregar el código de formulario al controlador de eventos del botón.</span><span class="sxs-lookup"><span data-stu-id="9a058-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="9a058-122">Agregar código de formulario al controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="9a058-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="9a058-123">En el controlador de eventos **OnClick**, escriba el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a058-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="9a058-p103">Observe que aparece una lista desplegable de Microsoft IntelliSense cada vez que se escribe un punto en la línea de código. La función completa del controlador de eventos debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="9a058-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
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
   > <span data-ttu-id="9a058-p104">[!NOTA] Como alternativa al método **Alert**, puede utilizar el método **MessageBox.Show** del espacio de nombres **System.Windows.Forms** para mostrar un cuadro de mensajes. Para ello, agregue una referencia al ensamblado System.Windows.Forms, agregue  `using System.Windows.Forms;` o  `Imports System.Windows.Forms` a las directivas al principio del archivo de código y, a continuación, escriba una línea de código como la siguiente:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="9a058-p104">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box. To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="9a058-128">Cambie a la ventana de modo de diseño de InfoPath y haga clic en el botón **Vista previa** de la ficha **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="9a058-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="9a058-129">En la ventana **Vista previa**, haga clic en el botón **Aviso**.</span><span class="sxs-lookup"><span data-stu-id="9a058-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="9a058-130">Aparecerá un cuadro de mensaje con el texto "Hello World".</span><span class="sxs-lookup"><span data-stu-id="9a058-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="9a058-131">El procedimiento siguiente muestra cómo agregar puntos de interrupción para depurar el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="9a058-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="9a058-132">Depurar el código del formulario</span><span class="sxs-lookup"><span data-stu-id="9a058-132">Debug form code</span></span>

1. <span data-ttu-id="9a058-133">En el editor de código, haga clic en la barra gris que se encuentra a la izquierda de esta línea:</span><span class="sxs-lookup"><span data-stu-id="9a058-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="9a058-134">Aparecerá un círculo rojo y la línea de código se resaltará para indicar que se hará una pausa en el tiempo de ejecución al llegar a este punto de interrupción en el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="9a058-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="9a058-135">En el menú **Depurar**, haga clic en **Iniciar depuración** (o presione F5).</span><span class="sxs-lookup"><span data-stu-id="9a058-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="9a058-136">En la ventana **Vista previa** de InfoPath, haga clic en el botón **Aviso**.</span><span class="sxs-lookup"><span data-stu-id="9a058-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="9a058-137">El foco se desplazará al editor de código y se resaltará la línea en la que se encuentra el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="9a058-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="9a058-138">En el menú **Depurar**, haga clic en **Paso a paso por procedimientos** (o presione Mayús+F8) para continuar depurando el código paso a paso.</span><span class="sxs-lookup"><span data-stu-id="9a058-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="9a058-p105">El código del método **Alert** se ejecuta y aparece el aviso "Hello World" en la ventana **Vista previa** de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a058-p105">The **Alert** method code is executed, and the "Hello World!" alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="9a058-141">Obtener el nombre del usuario actual</span><span class="sxs-lookup"><span data-stu-id="9a058-141">Getting the Current User's Name</span></span>

<span data-ttu-id="9a058-p106">Puede utilizar las clases de .NET Framework para obtener acceso a funciones de las que no se puede disponer con facilidad en las secuencias de comandos. En este ejemplo, aprenderá cómo utilizar las clases de .NET Framework para recuperar el nombre del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="9a058-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="9a058-144">Agregar un controlador de eventos OnLoad</span><span class="sxs-lookup"><span data-stu-id="9a058-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="9a058-145">Abra el proyecto HelloWorld de InfoPath que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="9a058-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="9a058-146">En la ficha **Ver**, haga clic en **Mostrar campos**.</span><span class="sxs-lookup"><span data-stu-id="9a058-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="9a058-147">Haga clic con el botón secundario en el nodo **myFields** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="9a058-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="9a058-148">En **Nombre**, escriba **empleado** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9a058-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="9a058-149">Arrastre el nodo **empleado** hasta la vista.</span><span class="sxs-lookup"><span data-stu-id="9a058-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="9a058-150">En la ficha **Programador**, haga clic en **Evento Al cargar (OnLoad)**.</span><span class="sxs-lookup"><span data-stu-id="9a058-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="9a058-p107">Se creará un controlador de eventos para el evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) y se desplazará el foco al editor de código. Se puede llamar al código de este controlador de eventos cada vez que se cargue el formulario. El procedimiento siguiente muestra cómo agregar código de formulario que recupere el nombre del usuario para el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="9a058-p107">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor. The code in this event handler will be called each time the form is loaded. The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="9a058-154">Agregar código de formulario</span><span class="sxs-lookup"><span data-stu-id="9a058-154">Add form code</span></span>

1. <span data-ttu-id="9a058-155">En el controlador de eventos **OnLoad**, escriba el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9a058-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
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

2. <span data-ttu-id="9a058-156">Compile el formulario y obtenga una vista previa del mismo.</span><span class="sxs-lookup"><span data-stu-id="9a058-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="9a058-157">El nombre de usuario debería aparecer ahora en el cuadro de texto Empleado.</span><span class="sxs-lookup"><span data-stu-id="9a058-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="9a058-158">Para obtener información acerca de cómo implementar una plantilla de formulario de código administrado, vea [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="9a058-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="9a058-159">Para obtener información acerca del modelo de objetos de InfoPath y las tareas de programación más comunes en las plantillas de formulario con código administrado que funcionan con el modelo de objetos compatible con InfoPath 2003, vea [Comprender el modelo de objetos de InfoPath 2003](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9a058-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a058-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a058-160">See also</span></span>

- [<span data-ttu-id="9a058-161">Utilizar código de limpieza e inicialización mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a058-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="9a058-162">Modelos de objetos compatibles con InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a058-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="9a058-163">Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a058-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
