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
# <a name="work-with-offline-solutions"></a>Trabajar con soluciones sin conexión

El modelo de objetos de InfoPath proporciona la propiedad [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , que permite al código del formulario comprobar si el equipo del usuario está conectado a la red. Comprobando el valor de la propiedad **MachineOnlineState**, el código puede llevar a cabo diferentes acciones en función del estado de la conexión. 
  
## <a name="using-the-machineonlinestate-property"></a>Uso de la propiedad MachineOnlineState

En el ejemplo siguiente, se muestra cómo se puede añadir al código una lógica que determine cómo enviar un formulario basándose en si el equipo del usuario está en línea o sin conexión.
  
En este ejemplo, se supone que se ha creado un formulario para enviar un informe de ventas que contiene un campo denominado período que especifica el mes y el año al que se refiere el informe. También asume que ya se ha definido una conexión de datos y la lógica para enviar el informe cuando el usuario está en línea. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Adición de una conexión de datos que envíe el formulario como datos adjuntos a un mensaje de correo electrónico

1. Cree una plantilla de formulario de InfoPath mediante la plantilla **En blanco (InfoPath Editor)**. 
    
2. En el modo de diseño de InfoPath, haga clic en **Conexiones de datos** en la ficha **Datos**. 
    
3. En el cuadro de diálogo **Conexiones de datos**, haga clic en **Agregar**.
    
4. En el **Asistente para la conexión de datos**, haga clic en **Enviar datos** y, a continuación, en **Siguiente**.
    
5. En la siguiente página del asistente, haga clic en **como mensaje de correo electrónico**y, a continuación, haga clic en **siguiente**.
    
6. En la siguiente página del asistente, escriba su dirección de correo electrónico en el cuadro **para** . 
    
7. En el cuadro **Asunto**, lleve a cabo la siguiente operación para combinar el período de ventas con el texto del informe de ventas: 
    
   1. Haga clic en el botón **Fórmula** junto al cuadro **Asunto**. 
      
   2. En el cuadro de diálogo **Insertar una fórmula**, haga clic en **Insertar una función**.
      
   3. En el cuadro de diálogo **Insertar una función**, haga clic en la opción **Texto** de la lista **Categorías** y, a continuación, haga doble clic en la opción **concat** de la lista **Funciones**. 
      
   4. Reemplace la primera instancia de **haga doble clic para insertar el campo** con el texto siguiente (incluyendo las comillas): 'Informe de ventas:' 
      
   5. Haga doble clic en la segunda instancia de **haga doble clic para insertar el campo**.
      
   6. En el cuadro de diálogo **Seleccionar una campo o grupo**, seleccione el campo período. 
      
   7. Elimine la última instancia de **haga doble clic para insertar el campo** y, a continuación, haga clic en **Aceptar**.
    
8. En el asistente, haga clic en **Siguiente**.
    
9. En la página siguiente del asistente, haga clic en el botón **Fórmula** situado junto al cuadro **Nombre de datos adjuntos**, a continuación, repita los pasos anteriores para crear la fórmula concat("Informe de ventas - ", periodo) y, finalmente, haga clic en **Siguiente**.
    
10. En la última página del asistente, escriba enviar correo electrónico en el cuadro **Escriba un nombre para esta conexión de datos** y, a continuación, haga clic en **Finalizar**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Agregar la lógica para enviar el formulario según el estado de la conexión del equipo del usuario

1. En el modo de diseño de InfoPath, haga clic en **Opciones de envío** en la ficha **Datos**. 
    
2. En el cuadro de diálogo **Opciones de envío**, haga clic en **Permitir a los usuarios enviar este formulario**, seleccione **Realizar una acción personalizada utilizando código** y haga clic en **Modificar código**.
    
3. Añada las dos funciones siguientes bajo el controlador de eventos [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) : 
    
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

4. Añada la siguiente instrucción **if** a la función de controlador de eventos [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) . 
    
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

### <a name="test-the-code"></a>Comprobación del código

1. En el menú **Depurar**, haga clic en **Iniciar depuración**.
    
2. Rellene el formulario.
    
3. Inicie Microsoft Internet Explorer.
    
4. En Internet Explorer, haga clic en **Trabajar sin conexión** en el menú **Archivo**. 
    
5. En InfoPath, haga clic en **Enviar**. Debe ver un mensaje que indica que el formulario se enviará como un mensaje de correo electrónico.
    
6. Haga clic en **Enviar**. Verá un mensaje que le notifica que el formulario se ha enviado sin conexión y que se enviará cuando se conecte a la red.
    
## <a name="see-also"></a>Vea también

- [Diseñar una plantilla de formulario para su uso sin conexión](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

