---
title: Valores de registro a un campo para la depuración
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Cuando se depura una plantilla de formulario de InfoPath, a menudo resulta útil registrar los valores directamente en un campo del formulario para crear un registro de los datos de depuración durante una sesión de prueba del formulario. En los siguientes procedimientos se muestra cómo crear un campo multilínea y, a continuación, agregar funciones auxiliares al código de formulario que permitan la depuración de datos en ese campo.
ms.openlocfilehash: f763e6b5d14fe5a5b4d9218af4acd0bc05a242af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815883"
---
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="06ae6-104">Valores de registro a un campo para la depuración</span><span class="sxs-lookup"><span data-stu-id="06ae6-104">Log values to a field for debugging</span></span>

<span data-ttu-id="06ae6-p102">Cuando se depura una plantilla de formulario de InfoPath, a menudo resulta útil registrar los valores directamente en un campo del formulario para crear un registro de los datos de depuración durante una sesión de prueba del formulario. En los siguientes procedimientos se muestra cómo crear un campo multilínea y, a continuación, agregar funciones auxiliares al código de formulario que permitan la depuración de datos en ese campo.</span><span class="sxs-lookup"><span data-stu-id="06ae6-p102">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="06ae6-107">Crear un campo de texto de varias líneas</span><span class="sxs-lookup"><span data-stu-id="06ae6-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="06ae6-108">Agregue un control **Cuadro de texto** al formulario y cambie su tamaño para que pueda mostrar varias líneas.</span><span class="sxs-lookup"><span data-stu-id="06ae6-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="06ae6-109">Haga clic con el botón secundario en el cuadro de texto, haga clic en **Propiedades de cuadro de texto** y active la casilla de verificación **Multilínea** en la ficha **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="06ae6-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="06ae6-110">Agregar funciones auxiliares para registrar información de depuración en el campo</span><span class="sxs-lookup"><span data-stu-id="06ae6-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="06ae6-111">En la ficha **Programador**, haga clic en **Editor de código** y guarde la plantilla de formulario si se le solicita.</span><span class="sxs-lookup"><span data-stu-id="06ae6-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="06ae6-112">En el Editor de código, agregue las tres funciones auxiliares siguientes a la clase pública en el archivo de código de formulario.</span><span class="sxs-lookup"><span data-stu-id="06ae6-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="06ae6-113">[!IMPORTANTE] Asegúrese de actualizar el conjunto de valores para la variable  `debugFieldXpath` de la función  `AddToDebugField` a la expresión XPath correcta para el archivo enlazado al control que ha creado en el primer procedimiento.</span><span class="sxs-lookup"><span data-stu-id="06ae6-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="06ae6-114">Cuando se utiliza Visual Basic, agregue `Imports Microsoft.VisualBasic.Constants` a las directivas en la parte superior del archivo de código de formulario.</span><span class="sxs-lookup"><span data-stu-id="06ae6-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="06ae6-115">Probar la función AddToDebugField</span><span class="sxs-lookup"><span data-stu-id="06ae6-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="06ae6-116">En la ficha **Programador**, haga clic en **Evento Loading** y agregue la siguiente línea de código al controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="06ae6-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="06ae6-117">En la ficha **Programador**, haga clic en **Evento View Switched** y agregue la siguiente línea de código al controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="06ae6-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="06ae6-118">En la ficha **Inicio**, haga clic en **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="06ae6-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="06ae6-p103">El campo de depuración mostrará dos entradas: una que indica que el formulario se ha cargado y otra que indica el nombre de la vista. En estos ejemplos se usan controladores de eventos para eventos que tienen lugar cuando se abre el formulario. Sin embargo, una vez cargado el formulario, se puede llamar a la función  `AddToDebugField` desde otros controladores de eventos además de cualquier otro código que se ejecute en el contexto del formulario.</span><span class="sxs-lookup"><span data-stu-id="06ae6-p103">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view. These examples use event handlers for events that occur as the form is opened. However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  

