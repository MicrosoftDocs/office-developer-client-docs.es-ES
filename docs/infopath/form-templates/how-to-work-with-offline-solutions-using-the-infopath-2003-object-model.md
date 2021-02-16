---
title: Trabajar con soluciones sin conexión mediante el modelo de objetos de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- solutions [infopath 2007], offline,offline solutions [InfoPath 2007], InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, offline solutions
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: El modelo de objetos compatible con InfoPath 2003 proporciona la propiedad MachineOnlineState del objeto Application , que permite al código del formulario comprobar si el equipo del usuario está conectado a la red. El código del formulario puede realizar acciones distintas según el estado de la conexión.
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429246"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="a57d0-105">Trabajar con soluciones sin conexión mediante el modelo de objetos de InfoPath</span><span class="sxs-lookup"><span data-stu-id="a57d0-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="a57d0-p102">El modelo de objetos compatible con InfoPath 2003 proporciona la propiedad [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) del objeto [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) , que permite al código del formulario comprobar si el equipo del usuario está conectado a la red. El código del formulario puede realizar acciones distintas según el estado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="a57d0-p102">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network. Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="a57d0-108">Uso de la propiedad MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="a57d0-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="a57d0-109">En el ejemplo siguiente, se muestra cómo se puede agregar al código una lógica que determine cómo enviar un formulario basándose en si el equipo del usuario está en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a57d0-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="a57d0-p103">En este ejemplo, se supone que se ha creado un formulario para enviar un informe de ventas que contiene un campo denominado "período" que especifica el mes y el año al que se refiere el informe. También asume que ya se ha definido una conexión de datos y la lógica para enviar el informe cuando el usuario está en línea.</span><span class="sxs-lookup"><span data-stu-id="a57d0-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="a57d0-112">Agregar una conexión de datos que envíe el formulario como datos adjuntos a un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a57d0-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="a57d0-113">Cree o abra una plantilla de formulario con código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="a57d0-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="a57d0-114">En el modo de diseño de InfoPath, en la ficha **Datos**, haga clic en **Conexiones de datos**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="a57d0-115">En el cuadro de diálogo **Conexiones de datos**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="a57d0-116">En el **Asistente para la conexión de datos**, haga clic en **Enviar datos** y, a continuación, en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="a57d0-117">En la página siguiente del asistente, haga clic en **Como mensaje de** correo electrónico y, a continuación, haga clic en **Siguiente.**</span><span class="sxs-lookup"><span data-stu-id="a57d0-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="a57d0-118">En la siguiente página del asistente, escriba su dirección de correo electrónico en el **cuadro Para.**</span><span class="sxs-lookup"><span data-stu-id="a57d0-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="a57d0-119">En el cuadro **Asunto**, lleve a cabo la siguiente operación para combinar el período de ventas con el texto del informe de ventas:</span><span class="sxs-lookup"><span data-stu-id="a57d0-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="a57d0-120">Haga clic en el botón **Fórmula** junto al cuadro **Asunto**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="a57d0-121">En el cuadro de diálogo **Insertar una fórmula**, haga clic en **Insertar una función**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="a57d0-122">En el cuadro de diálogo **Insertar una función**, haga clic en la opción **Texto** de la lista **Categorías** y, a continuación, haga doble clic en la opción **concat** de la lista **Funciones**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="a57d0-123">Reemplace la primera instancia de **haga doble clic para insertar el campo** con el texto siguiente (incluyendo las comillas): 'Informe de ventas:'</span><span class="sxs-lookup"><span data-stu-id="a57d0-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="a57d0-124">Haga doble clic en la segunda instancia de **haga doble clic para insertar el campo**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="a57d0-125">En el cuadro de diálogo **Seleccionar una campo o grupo**, seleccione el campo período.</span><span class="sxs-lookup"><span data-stu-id="a57d0-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="a57d0-126">Elimine la última instancia de **haga doble clic para insertar el campo** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="a57d0-127">En el asistente, haga clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="a57d0-128">En la página siguiente del asistente, escriba "Enviar correo electrónico" en el cuadro Escribir un nombre para esta conexión de datos y, **a** continuación, haga clic **en Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="a57d0-129">Añadir la lógica para enviar el formulario según el estado de la conexión del equipo del usuario</span><span class="sxs-lookup"><span data-stu-id="a57d0-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="a57d0-130">En el modo de diseño de InfoPath, en la ficha **Datos**, haga clic en **Opciones de envío**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="a57d0-131">En el cuadro de diálogo **Opciones de envío**, haga clic en **Permitir a los usuarios enviar este formulario** y, a continuación, seleccione **Realizar una acción personalizada utilizando código**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="a57d0-132">Haga clic en el botón **Modificar código**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="a57d0-133">Añada las dos funciones siguientes bajo el controlador de eventos [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a57d0-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
   ```cs
    public void OnlineSubmit(DocReturnEvent e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmitX(DocReturnEvent e)
    {
      // Access and submit to the email adapter.
      DataAdaptersCollection myDataAdapters = 
          thisXDocument.DataAdapters;
      EmailAdapterObject submitAdapter = 
          (EmailAdapterObject) myDataAdapters["Email Submit"];
      submitAdapter.Submit();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder message = 
      new System.Text.StringBuilder();
      message.Append("You submitted your Sales Report offline. ");
      message.Append("Your Sales Report is in your outbox ");
      message.Append("and will be submitted when you connect to ");
      message.Append("the network.");
        thisXDocument.UI.Alert(message.ToString());
      // The submission was successful.
      e.ReturnStatus = true;
    }
   ```

5. <span data-ttu-id="a57d0-134">Añada la siguiente instrucción **if** a la función de controlador de eventos **OnSubmitRequest**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
   ```cs
    // Check the computer's connection state.
    if (thisApplication.MachineOnlineState==XdMachineOnlineState.xdOnline)
    {
        OnlineSubmit(e);
    }
    else
    {
        OfflineSubmit(e);
    }
   ```

### <a name="test-the-code"></a><span data-ttu-id="a57d0-135">Probar el código</span><span class="sxs-lookup"><span data-stu-id="a57d0-135">Test the code</span></span>

1. <span data-ttu-id="a57d0-136">En InfoPath Designer, haga clic en **Vista previa** en la ficha **Inicio**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="a57d0-137">Rellene el formulario.</span><span class="sxs-lookup"><span data-stu-id="a57d0-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="a57d0-138">Inicie Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a57d0-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="a57d0-139">En Internet Explorer, haga clic en **Trabajar sin conexión** en el menú **Archivo**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="a57d0-140">En InfoPath, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="a57d0-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="a57d0-141">Debería ver un mensaje que indica que el formulario se enviará como un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a57d0-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="a57d0-p105">Haga clic en **Enviar**. Verá un mensaje que le notificará que el formulario se ha enviado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a57d0-p105">Click **Send**. You should see a message stating that the form has been submitted offline.</span></span>
    

