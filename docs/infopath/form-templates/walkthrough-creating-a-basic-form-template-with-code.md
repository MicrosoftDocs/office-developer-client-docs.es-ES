---
title: 'Tutorial: Crear una plantilla de formulario básica con código'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- plantillas de formulario [infopath 2007], crear código administrado, plantillas de formulario de código administrado [InfoPath 2007], crear, plantillas formulario [InfoPath 2007], tutoriales, InfoPath 2007, tutoriales
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: En Microsoft InfoPath, puede escribir lógica empresarial en Visual Basic o C# si abre una plantilla en el diseñador de InfoPath y, a continuación, usa uno de los comandos de la interfaz de usuario para agregar un controlador de eventos, que abrirá el entorno de desarrollo de Visual Studio 2012 para que se escriba el código.
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299737"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="c5f1d-104">Tutorial: Crear una plantilla de formulario básica con código</span><span class="sxs-lookup"><span data-stu-id="c5f1d-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="c5f1d-p101">En Microsoft InfoPath, puede escribir lógica empresarial en Visual Basic o C# si abre una plantilla en el diseñador de InfoPath y, a continuación, usa uno de los comandos de la interfaz de usuario para agregar un controlador de eventos, que abrirá el entorno de desarrollo de Visual Studio 2012 para que se escriba el código. De manera predeterminada, los proyectos de plantilla de formulario creados con Visual Studio 2012 funcionan con el nuevo modelo de objetos de código administrado proporcionado por el espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p101">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code. By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="c5f1d-p102">Este tutorial muestra en primer lugar cómo crear una sencilla aplicación denominada "Hola a todos" utilizando C# o Visual Basic en el entorno de desarrollo de Visual Studio 2012. El tutorial termina con un ejemplo de código que muestra cómo usar la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la clase [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar el nombre del usuario actual y rellenar un control de **Cuadro de texto** con ese valor.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p102">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment. The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="c5f1d-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c5f1d-109">Prerequisites</span></span>

<span data-ttu-id="c5f1d-110">Para llevar a cabo este tutorial utilizando el entorno de desarrollo de Visual Studio 2012, necesitará:</span><span class="sxs-lookup"><span data-stu-id="c5f1d-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="c5f1d-111">Microsoft InfoPath con Visual Studio 2012 instalado.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="c5f1d-112">"Hola a todos" en Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="c5f1d-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="c5f1d-113">En el siguiente tutorial, aprenderá a escribir código en el entorno de desarrollo de Visual Studio 2012 para hacer que se muestre un sencillo cuadro de diálogo de alerta. Para ello, escribirá un controlador de eventos para el evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) de la clase [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , que está asociada al control **Botón**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="c5f1d-114">Crear un nuevo proyecto y especificar un lenguaje de programación</span><span class="sxs-lookup"><span data-stu-id="c5f1d-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="c5f1d-115">Inicie el diseñador de InfoPath y a continuación haga doble clic en la plantilla de formulario **En blanco (InfoPath Editor)**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="c5f1d-116">Para especificar el lenguaje de programación que desea usar, haga clic en el **botón de Office**, haga clic en **Opciones de formulario**, haga clic en **Programación** en la lista **Categoría** y a continuación seleccione **Visual Basic** o **C#** de la lista desplegable **Lenguaje del código de la plantilla de formulario**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="c5f1d-p103">Las demás opciones de lenguaje de programación de la lista desplegable **Lenguaje del código de la plantilla de formulario** proporcionan compatibilidad con versiones anteriores de InfoPath. Las opciones **C# (compatible con InfoPath 2007)** y **Visual Basic (compatible con InfoPath 2007)** funcionarán con los procedimientos de este tema. Sin embargo, para utilizar las opciones **C# (compatible con InfoPath 2003)** y **Visual Basic (compatible con InfoPath 2003)**, vea [Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p103">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath. The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic. However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="c5f1d-120">Ya está todo preparado para agregar un control **Botón** y crear su controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="c5f1d-121">Agregar un control Botón y un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="c5f1d-122">En el grupo **Controles**, haga clic en el control **Botón** para agregarlo al formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="c5f1d-p104">Haga doble clic en el control **Botón**, escriba Hola para la propiedad **Etiqueta** en la ficha **Propiedades** de la cinta y a continuación haga clic en **Código personalizado**. Cuando se le pida, guarde el formulario con el nombre "Hola a todos".</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p104">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**. When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="c5f1d-125">Así se abrirá el entorno de **Visual Studio Tools for Applications** con el cursor situado en el controlador de eventos para el evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) del control **Botón**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="c5f1d-126">Ya está todo preparado para agregar el código de formulario al controlador de eventos del botón.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="c5f1d-127">Agregue el código de "Hola a todos" al controlador de eventos y obtenga una vista previa del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="c5f1d-128">En el esqueleto del controlador de eventos, escriba:</span><span class="sxs-lookup"><span data-stu-id="c5f1d-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="c5f1d-129">El código de la plantilla de formulario debe tener un aspecto parecido al siguiente:</span><span class="sxs-lookup"><span data-stu-id="c5f1d-129">The code for your form template should look similar to the following:</span></span>
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. <span data-ttu-id="c5f1d-130">Cambie a la ventana de diseñador de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="c5f1d-131">Haga clic en el botón **Vista previa** de la ficha **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="c5f1d-132">Haga clic en el botón Hola del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="c5f1d-133">Aparecerá un cuadro de mensaje con el texto "Hola a todos".</span><span class="sxs-lookup"><span data-stu-id="c5f1d-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="c5f1d-134">El procedimiento siguiente muestra cómo agregar puntos de interrupción para depurar el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="c5f1d-135">Depurar el código del formulario</span><span class="sxs-lookup"><span data-stu-id="c5f1d-135">Debug form code</span></span>

1. <span data-ttu-id="c5f1d-136">Cambie a la ventana de Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="c5f1d-137">Haga clic en la barra gris situada a la izquierda de la línea:</span><span class="sxs-lookup"><span data-stu-id="c5f1d-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="c5f1d-138">Aparecerá un círculo rojo y la línea de código se resaltará para indicar que, en tiempo de ejecución, se hará una pausa al llegar a este punto de interrupción en el código del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="c5f1d-139">En el menú **Depurar** haga clic en **Iniciar depuración** (o presione F5).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="c5f1d-140">En la ventana **Vista previa** de InfoPath, haga clic en el botón Hola del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="c5f1d-141">El foco se desplazará al editor de código de Visual Studio 2012 y se resaltará la línea en la que se encuentra el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="c5f1d-142">En el menú **Depurar**, haga clic en **Paso a paso por procedimientos** (o presione Mayús+F8) para continuar paso a paso por los procedimientos del código.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="c5f1d-p105">Se ejecuta el código del controlador de eventos y se muestra el mensaje "Hola a todos".</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="c5f1d-145">Haga clic en **Aceptar** para volver al editor de código de Visual Studio de 2012 y después haga clic en **Detener depuración** en el menú **Depurar** (o presione Ctrl+Alt+Interrumpir).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="c5f1d-146">Obtener el nombre del usuario actual</span><span class="sxs-lookup"><span data-stu-id="c5f1d-146">Getting the current user's name</span></span>

<span data-ttu-id="c5f1d-147">En el ejemplo siguiente, aprenderá a utilizar la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la clase [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar el nombre del usuario actual y rellenar el valor de un control **Cuadro de texto** mediante un controlador de eventos para el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5f1d-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="c5f1d-148">El control **Cuadro de texto** se rellena usando una instancia de la clase [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para escribir el nombre del usuario actual en el nodo XML al que está enlazado el control.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="c5f1d-p106">En primer lugar se llama a la propiedad [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para recuperar una instancia de la clase [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa el documento XML subyacente del formulario. A continuación, el objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) llama al método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , que crea el objeto **XPathNavigator** y lo coloca en el nodo raíz del origen de datos principal del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p106">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form. The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="c5f1d-p107">Se llama al método [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) de la clase **XPathNavigator** para seleccionar el campo empleado en el origen de datos del formulario. Finalmente, se llama al método [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) para establecer el valor del campo con la propiedad [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5f1d-p107">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source. Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="c5f1d-153">Para obtener más información sobre cómo trabajar con **System.Xml** en plantillas de formulario de código administrado, vea [Trabajar con las clases XPathNavigator y XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-153">For more information on working with **System.Xml** in managed code form templates, see [Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="c5f1d-154">Agregar un cuadro controlador de eventos de carga</span><span class="sxs-lookup"><span data-stu-id="c5f1d-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="c5f1d-155">Abra la plantilla de formulario "Hola a todos" que ha creado en el tutorial anterior en el diseñador de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="c5f1d-156">En la ficha **Ver**, seleccione **Mostrar campos**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="c5f1d-157">Haga clic con el botón secundario en la carpeta **misCampos** y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="c5f1d-158">En **Nombre**, escriba empleado y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="c5f1d-159">Arrastre el campo empleado a la vista.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="c5f1d-160">En la ficha **Programador**, haga clic en **Evento Loading**.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="c5f1d-161">Así se creará un controlador de eventos para el evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) y el foco se desplazará a dicho controlador de eventos en el editor de código.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="c5f1d-162">En el editor de código, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c5f1d-162">In the code editor, type the following:</span></span>
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. <span data-ttu-id="c5f1d-163">Cambie a la ventana de diseño de formulario de InfoPath y a continuación haga clic en el botón **Vista previa** de la ficha **Inicio** para obtener la vista previa del formulario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="c5f1d-164">El campo empleado debe rellenarse automáticamente con el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="c5f1d-165">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="c5f1d-165">Next steps</span></span>

- <span data-ttu-id="c5f1d-166">Para obtener información sobre cómo trabajar con controladores de eventos para otros controles y eventos, vea [Agregar un controlador de eventos](how-to-add-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-166">For information about working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="c5f1d-167">Para obtener información sobre la vista previa y la depuración de código de las plantillas de formulario, vea [Obtener una vista previa y depurar plantillas de formulario de InfoPath con código](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-167">For more information about previewing and debugging code in form templates, see [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="c5f1d-168">Para obtener información sobre cómo implementar plantillas de formulario con código administrado, vea [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-168">For information about how to deploy a managed-code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="c5f1d-169">Para obtener información sobre el modelo de objetos de InfoPath y las tareas de programación más comunes en la plantillas de formulario con código administrado, vea [Comprender el modelo de objetos de InfoPath y las tareas de programación más comunes](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="c5f1d-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5f1d-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5f1d-170">See also</span></span>

- [<span data-ttu-id="c5f1d-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="c5f1d-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

