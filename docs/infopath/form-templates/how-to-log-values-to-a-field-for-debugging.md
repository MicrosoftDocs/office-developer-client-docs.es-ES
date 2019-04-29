---
title: Registrar valores en un campo para la depuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Cuando se depura una plantilla de formulario de InfoPath, a menudo resulta útil registrar los valores directamente en un campo del formulario para crear un registro de los datos de depuración durante una sesión de prueba del formulario. En los siguientes procedimientos se muestra cómo crear un campo multilínea y, a continuación, agregar funciones auxiliares al código de formulario que permitan la depuración de datos en ese campo.
ms.openlocfilehash: 28f2a1ad3c13aefd9f898bdf397c9103df98d3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431816"
---
# <a name="log-values-to-a-field-for-debugging"></a>Registrar valores en un campo para la depuración

Cuando se depura una plantilla de formulario de InfoPath, a menudo resulta útil registrar los valores directamente en un campo del formulario para crear un registro de los datos de depuración durante una sesión de prueba del formulario. En los siguientes procedimientos se muestra cómo crear un campo multilínea y, a continuación, agregar funciones auxiliares al código de formulario que permitan la depuración de datos en ese campo.
  
## <a name="create-a-multi-line-text-field"></a>Crear un campo de texto de varias líneas

1. Agregue un control **Cuadro de texto** al formulario y cambie su tamaño para que pueda mostrar varias líneas. 
    
2. Haga clic con el botón secundario en el cuadro de texto, haga clic en **Propiedades de cuadro de texto** y active la casilla de verificación **Multilínea** en la ficha **Mostrar**. 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Agregar funciones auxiliares para registrar información de depuración en el campo

1. En la ficha **Programador**, haga clic en **Editor de código** y guarde la plantilla de formulario si se le solicita.
    
2. En el Editor de código, agregue las tres funciones auxiliares siguientes a la clase pública en el archivo de código de formulario.
    
   > [!IMPORTANT]
   > [!IMPORTANTE] Asegúrese de actualizar el conjunto de valores para la variable  `debugFieldXpath` de la función  `AddToDebugField` a la expresión XPath correcta para el archivo enlazado al control que ha creado en el primer procedimiento. 
  
    ```cs
        private void AddToDebugField(string valueToAdd)
        {
            // Update the value of debugFieldXpath to the XPath of the
            // multi-line field where you want to log debug information.
            string debugFieldXpath = "/my:myFields/my:field1";
            string headerLine = "----------------- " + DateTime.Now + 
                " -----------------" + "\r\n";
            SetDebugFieldValue(debugFieldXpath, headerLine + valueToAdd + 
                "\r\n" + GetDebugFieldValue(debugFieldXpath));
        }
        private string GetDebugFieldValue(string xpath)
        {
            return this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).Value;
        }
        private void SetDebugFieldValue(string xpath, string value)
        {
            this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).SetValue(value);
        }
    ```

    ```vb
        Private Sub AddToDebugField(ByVal valueToAdd As String)
            ' Update the value of debugFieldXpath to the XPath of the 
            ' multi-line field where you want to log debug information.
            Dim debugFieldXpath As String = "/my:myFields/my:field1"
            Dim headerLine As String = "----------------- " _
                &amp; DateTime.Now &amp; " -----------------" &amp; vbCrLf
            SetDebugFieldValue(debugFieldXpath, (headerLine &amp; valueToAdd &amp; vbCrLf) _
                &amp; GetDebugFieldValue(debugFieldXpath))
        End Sub
        Private Function GetDebugFieldValue(ByVal xpath As String) As String
            Return Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).Value
        End Function
        Private Sub SetDebugFieldValue(ByVal xpath As String, ByVal value As String)
            Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).SetValue(value)
        End Sub
    ```

> [!NOTE] 
> Cuando use Visual Basic, agregue `Imports Microsoft.VisualBasic.Constants` a las directivas que se encuentra en la parte superior del archivo de código del formulario. 
  
## <a name="test-the-addtodebugfield-function"></a>Probar la función AddToDebugField

1. En la ficha **Programador**, haga clic en **Evento Loading** y agregue la siguiente línea de código al controlador de eventos.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. En la ficha **Programador**, haga clic en **Evento View Switched** y agregue la siguiente línea de código al controlador de eventos.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. En la ficha **Inicio**, haga clic en **Vista previa**.
    
   El campo de depuración mostrará dos entradas: una que indica que el formulario se ha cargado y otra que indica el nombre de la vista. En estos ejemplos se usan controladores de eventos para eventos que tienen lugar cuando se abre el formulario. Sin embargo, una vez cargado el formulario, se puede llamar a la función  `AddToDebugField` desde otros controladores de eventos además de cualquier otro código que se ejecute en el contexto del formulario. 
  

