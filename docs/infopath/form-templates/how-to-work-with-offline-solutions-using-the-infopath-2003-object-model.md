---
title: Trabajar con soluciones sin conexión con el modelo de objetos de InfoPath
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
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Trabajar con soluciones sin conexión con el modelo de objetos de InfoPath

El modelo de objetos compatible con InfoPath 2003 proporciona la propiedad [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) del objeto [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) , que permite al código del formulario comprobar si el equipo del usuario está conectado a la red. El código del formulario puede realizar acciones distintas según el estado de la conexión. 
  
## <a name="using-the-machineonlinestate-property"></a>Uso de la propiedad MachineOnlineState

En el ejemplo siguiente, se muestra cómo se puede agregar al código una lógica que determine cómo enviar un formulario basándose en si el equipo del usuario está en línea o sin conexión.
  
En este ejemplo, se supone que se ha creado un formulario para enviar un informe de ventas que contiene un campo denominado "período" que especifica el mes y el año al que se refiere el informe. También asume que ya se ha definido una conexión de datos y la lógica para enviar el informe cuando el usuario está en línea.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Agregar una conexión de datos que envíe el formulario como datos adjuntos a un mensaje de correo electrónico

1. Cree o abra una plantilla de formulario con código administrado de InfoPath.
    
2. En el modo de diseño de InfoPath, en la ficha **Datos**, haga clic en **Conexiones de datos**.
    
3. En el cuadro de diálogo **Conexiones de datos**, haga clic en **Agregar**.
    
4. En el **Asistente para la conexión de datos**, haga clic en **Enviar datos** y, a continuación, en **Siguiente**.
    
5. En la página siguiente del asistente, haga clic **en Como mensaje de** correo electrónico y, a continuación, haga clic en **Siguiente**.
    
6. En la siguiente página del asistente, escriba su dirección de correo electrónico en el **cuadro Para.** 
    
7. En el cuadro **Asunto**, lleve a cabo la siguiente operación para combinar el período de ventas con el texto del informe de ventas: 
    
   1. Haga clic en el botón **Fórmula** junto al cuadro **Asunto**. 
      
   2. En el cuadro de diálogo **Insertar una fórmula**, haga clic en **Insertar una función**.
      
   3. En el cuadro de diálogo **Insertar una función**, haga clic en la opción **Texto** de la lista **Categorías** y, a continuación, haga doble clic en la opción **concat** de la lista **Funciones**. 
      
   4. Reemplace la primera instancia de **haga doble clic para insertar el campo** con el texto siguiente (incluyendo las comillas): 'Informe de ventas:' 
      
   5. Haga doble clic en la segunda instancia de **haga doble clic para insertar el campo**.
      
   6. En el cuadro de diálogo **Seleccionar una campo o grupo**, seleccione el campo período. 
      
   7. Elimine la última instancia de **haga doble clic para insertar el campo** y, a continuación, haga clic en **Aceptar**.
    
8. En el asistente, haga clic en **Siguiente**.
    
9. En la página siguiente del asistente, escriba "Enviar correo electrónico" en el cuadro Escriba un nombre para esta conexión de datos y, **a** continuación, haga clic en **Finalizar**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Añadir la lógica para enviar el formulario según el estado de la conexión del equipo del usuario

1. En el modo de diseño de InfoPath, en la ficha **Datos**, haga clic en **Opciones de envío**.
    
2. En el cuadro de diálogo **Opciones de envío**, haga clic en **Permitir a los usuarios enviar este formulario** y, a continuación, seleccione **Realizar una acción personalizada utilizando código**.
    
3. Haga clic en el botón **Modificar código**. 
    
4. Añada las dos funciones siguientes bajo el controlador de eventos [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) . 
    
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

5. Añada la siguiente instrucción **if** a la función de controlador de eventos **OnSubmitRequest**. 
    
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

### <a name="test-the-code"></a>Probar el código

1. En InfoPath Designer, haga clic en **Vista previa** en la ficha **Inicio**. 
    
2. Rellene el formulario.
    
3. Inicie Microsoft Internet Explorer.
    
4. En Internet Explorer, haga clic en **Trabajar sin conexión** en el menú **Archivo**. 
    
5. En InfoPath, haga clic en **Enviar**. Debería ver un mensaje que indica que el formulario se enviará como un mensaje de correo electrónico.
    
6. Haga clic en **Enviar**. Verá un mensaje que le notificará que el formulario se ha enviado sin conexión.
    

