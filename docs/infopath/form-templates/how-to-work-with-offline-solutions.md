---
title: Trabajar con soluciones sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- offline solutions [infopath 2007],solutions [InfoPath 2007], offline,InfoPath 2007, offline solutions
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: El modelo de objetos de InfoPath proporciona la propiedad MachineOnlineState de la clase Application , que permite al código del formulario comprobar si el equipo del usuario está conectado a la red. Comprobando el valor de la propiedad MachineOnlineState, el código puede llevar a cabo diferentes acciones en función del estado de la conexión.
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299821"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="ae145-105">Trabajar con soluciones sin conexión</span><span class="sxs-lookup"><span data-stu-id="ae145-105">Work with offline solutions</span></span>

<span data-ttu-id="ae145-p102">El modelo de objetos de InfoPath proporciona la propiedad [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , que permite al código del formulario comprobar si el equipo del usuario está conectado a la red. Comprobando el valor de la propiedad **MachineOnlineState**, el código puede llevar a cabo diferentes acciones en función del estado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="ae145-p102">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network. By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="ae145-108">Uso de la propiedad MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="ae145-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="ae145-109">En el ejemplo siguiente, se muestra cómo se puede añadir al código una lógica que determine cómo enviar un formulario basándose en si el equipo del usuario está en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ae145-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="ae145-p103">En este ejemplo, se supone que se ha creado un formulario para enviar un informe de ventas que contiene un campo denominado período que especifica el mes y el año al que se refiere el informe. También asume que ya se ha definido una conexión de datos y la lógica para enviar el informe cuando el usuario está en línea.</span><span class="sxs-lookup"><span data-stu-id="ae145-p103">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="ae145-112">Adición de una conexión de datos que envíe el formulario como datos adjuntos a un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="ae145-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="ae145-113">Cree una plantilla de formulario de InfoPath mediante la plantilla **En blanco (InfoPath Editor)**.</span><span class="sxs-lookup"><span data-stu-id="ae145-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="ae145-114">En el modo de diseño de InfoPath, haga clic en **Conexiones de datos** en la ficha **Datos**.</span><span class="sxs-lookup"><span data-stu-id="ae145-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="ae145-115">En el cuadro de diálogo **Conexiones de datos**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ae145-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="ae145-116">En el **Asistente para la conexión de datos**, haga clic en **Enviar datos** y, a continuación, en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ae145-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="ae145-117">En la siguiente página del asistente, haga clic en **como mensaje de correo electrónico**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ae145-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="ae145-118">En la siguiente página del asistente, escriba su dirección de correo electrónico en el cuadro **para** .</span><span class="sxs-lookup"><span data-stu-id="ae145-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="ae145-119">En el cuadro **Asunto**, lleve a cabo la siguiente operación para combinar el período de ventas con el texto del informe de ventas:</span><span class="sxs-lookup"><span data-stu-id="ae145-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="ae145-120">Haga clic en el botón **Fórmula** junto al cuadro **Asunto**.</span><span class="sxs-lookup"><span data-stu-id="ae145-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="ae145-121">En el cuadro de diálogo **Insertar una fórmula**, haga clic en **Insertar una función**.</span><span class="sxs-lookup"><span data-stu-id="ae145-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="ae145-122">En el cuadro de diálogo **Insertar una función**, haga clic en la opción **Texto** de la lista **Categorías** y, a continuación, haga doble clic en la opción **concat** de la lista **Funciones**.</span><span class="sxs-lookup"><span data-stu-id="ae145-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="ae145-123">Reemplace la primera instancia de **haga doble clic para insertar el campo** con el texto siguiente (incluyendo las comillas): 'Informe de ventas:'</span><span class="sxs-lookup"><span data-stu-id="ae145-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="ae145-124">Haga doble clic en la segunda instancia de **haga doble clic para insertar el campo**.</span><span class="sxs-lookup"><span data-stu-id="ae145-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="ae145-125">En el cuadro de diálogo **Seleccionar una campo o grupo**, seleccione el campo período.</span><span class="sxs-lookup"><span data-stu-id="ae145-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="ae145-126">Elimine la última instancia de **haga doble clic para insertar el campo** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ae145-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="ae145-127">En el asistente, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ae145-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="ae145-128">En la página siguiente del asistente, haga clic en el botón **Fórmula** situado junto al cuadro **Nombre de datos adjuntos**, a continuación, repita los pasos anteriores para crear la fórmula concat("Informe de ventas - ", periodo) y, finalmente, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="ae145-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="ae145-129">En la última página del asistente, escriba enviar correo electrónico en el cuadro **Escriba un nombre para esta conexión de datos** y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="ae145-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="ae145-130">Agregar la lógica para enviar el formulario según el estado de la conexión del equipo del usuario</span><span class="sxs-lookup"><span data-stu-id="ae145-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="ae145-131">En el modo de diseño de InfoPath, haga clic en **Opciones de envío** en la ficha **Datos**.</span><span class="sxs-lookup"><span data-stu-id="ae145-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="ae145-132">En el cuadro de diálogo **Opciones de envío**, haga clic en **Permitir a los usuarios enviar este formulario**, seleccione **Realizar una acción personalizada utilizando código** y haga clic en **Modificar código**.</span><span class="sxs-lookup"><span data-stu-id="ae145-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="ae145-133">Añada las dos funciones siguientes bajo el controlador de eventos [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) :</span><span class="sxs-lookup"><span data-stu-id="ae145-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
   ```cs
    public void OnlineSubmit(SubmitEventArgs e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmit(SubmitEventArgs e)
    {
      // Access and submit to the email connection.
      DataConnectionCollection myDataConnections =
          this.DataConnections;
      EmailSubmitConnection submitConnection =
          (EmailSubmitConnection)myDataConnections["Email Submit"];
      submitConnection.Execute();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder myMessage = 
          new System.Text.StringBuilder();
      myMessage.Append("You submitted your Sales Report offline. ");
      myMessage.Append("Your Sales Report is in your outbox ");
      myMessage.Append("and will be submitted when you connect to ");
      myMessage.Append("the network.");
        MessageBox.Show(myMessage.ToString());
      // The submission was successful.
      e.CancelableArgs.Cancel = false;
    }
   ```

   ```vb
    Public Sub OnlineSubmit(ByVal e As SubmitEventArgs)
      ' Logic for submitting online goes here.
    End Sub
    Public Sub OfflineSubmit(ByVal e As SubmitEventArgs)
      ' Access and submit to the email connection.
      Dim myDataConnections As DataConnectionCollection = _
          Me.DataConnections
      Dim submitConnection As EmailSubmitConnection = _
          DirectCast(myDataConnections("Email Submit"), _
          EmailSubmitConnection)
      submitConnection.Execute
      ' Notify the user that the form was submitted offline.
      Dim myMessage As System.Text.StringBuilder = _
          New System.Text.StringBuilder()
      myMessage.Append("You submitted your Sales Report offline. ")
      myMessage.Append("Your Sales Report is in your outbox ")
      myMessage.Append("and will be submitted when you connect to ")
      myMessage.Append("the network.")
        MessageBox.Show(myMessage.ToString())
      ' The submission was successful.
      e.CancelableArgs.Cancel = False
    End Sub
   ```

4. <span data-ttu-id="ae145-134">Añada la siguiente instrucción **if** a la función de controlador de eventos [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae145-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
   ```cs
    // Check the computer's connection state.
    if (this.Application.MachineOnlineState == MachineState.Online)
    {
      OnlineSubmit(e);
    }
    else
    {
      OfflineSubmit(e);
    }
   ```

   ```vb
    ' Check the computer's connection state.
    If (Me.Application.MachineOnlineState = MachineState.Online) Then
      OnlineSubmit(e)
    Else
    {
      OfflineSubmit(e)
    End If
   ```

### <a name="test-the-code"></a><span data-ttu-id="ae145-135">Comprobación del código</span><span class="sxs-lookup"><span data-stu-id="ae145-135">Test the code</span></span>

1. <span data-ttu-id="ae145-136">En el menú **Depurar**, haga clic en **Iniciar depuración**.</span><span class="sxs-lookup"><span data-stu-id="ae145-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="ae145-137">Rellene el formulario.</span><span class="sxs-lookup"><span data-stu-id="ae145-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="ae145-138">Inicie Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ae145-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="ae145-139">En Internet Explorer, haga clic en **Trabajar sin conexión** en el menú **Archivo**.</span><span class="sxs-lookup"><span data-stu-id="ae145-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="ae145-140">En InfoPath, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="ae145-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="ae145-141">Debe ver un mensaje que indica que el formulario se enviará como un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ae145-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="ae145-p105">Haga clic en **Enviar**. Verá un mensaje que le notifica que el formulario se ha enviado sin conexión y que se enviará cuando se conecte a la red.</span><span class="sxs-lookup"><span data-stu-id="ae145-p105">Click **Send**. You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae145-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae145-144">See also</span></span>

- [<span data-ttu-id="ae145-145">Diseñar una plantilla de formulario para su uso sin conexión</span><span class="sxs-lookup"><span data-stu-id="ae145-145">Design a form template for offline use</span></span>](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

