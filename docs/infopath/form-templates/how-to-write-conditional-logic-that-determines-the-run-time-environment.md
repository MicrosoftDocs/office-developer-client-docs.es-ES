---
title: Escribir lógica condicional que deTermine el entorno en tiempo de ejecución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- running in infopath [infopath 2007],run-time environment [InfoPath 2007],running in browser [InfoPath 2007],InfoPath 2007, determining run-time environment
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: La propiedad Environment de la clase Application obtiene una referencia a un objeto Environment , que se puede usar para determinar el entorno en tiempo de ejecución (InfoPath, explorador web o explorador móvil) que se utilizó para abrir el formulario.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408603"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="55ce1-104">Escribir lógica condicional que deTermine el entorno en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="55ce1-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="55ce1-105">La propiedad [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtiene una referencia a un objeto [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , que se puede usar para determinar el entorno en tiempo de ejecución (InfoPath, explorador web o explorador móvil) que se utilizó para abrir el formulario.</span><span class="sxs-lookup"><span data-stu-id="55ce1-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="55ce1-106">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55ce1-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="55ce1-107">Determinar el entorno en tiempo de ejecución en el que se ejecuta un formulario</span><span class="sxs-lookup"><span data-stu-id="55ce1-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="55ce1-p101">La clase [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) proporciona las propiedades [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) y [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , que le permiten determinar el entorno de edición que se utilizó para abrir una plantilla de formulario. Si las dos propiedades devuelven **false**, la plantilla se abrió en el editor de Microsoft InfoPath. Si una de las propiedades devuelve **true**, se abrió desde una biblioteca de documentos configurada adecuadamente en Microsoft SharePoint Server 2010 con InfoPath Forms Services en el programa correspondiente a la propiedad: un explorador web (propiedad [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ) o un explorador móvil (propiedad [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="55ce1-p101">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template. If both properties return **false**, the form template was opened in the Microsoft InfoPath editor. If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="55ce1-p102">En el ejemplo siguiente, si el formulario se abre en un explorador o en un explorador móvil, el valor del campo1 (que está enlazado a un control **Cuadro de texto**) se establece como una cadena para indicar el entorno en tiempo de ejecución en que se abrió el formulario. Si el formulario se abrió en InfoPath, el método **System.Windows.Forms.MessageBox.Show** (que no está disponible cuando un formulario se ejecuta en un explorador) se utiliza para mostrar un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="55ce1-p102">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in. If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="55ce1-p103">[!IMPORTANTE] Cuando se crea una plantilla de formulario para el siguiente ejemplo de código, seleccione la plantilla **En blanco** de la ficha **Nuevo** en la vista Backstage. (También puede seleccionar **Formulario de explorador web** de la lista desplegable **Tipo de formulario** bajo la categoría **Compatibilidad** del cuadro de diálogo **Opciones de formulario**). Para que se admita la clase **MessageBox**, agregue una referencia a **System.Windows.Forms** en la ficha **NET** del cuadro de diálogo **Agregar referencia** en Visual Studio 2012 y, después, agregue una directiva **using** o **Imports** para **System.Windows.Forms** en la sección de declaraciones del módulo de código del formulario.</span><span class="sxs-lookup"><span data-stu-id="55ce1-p103">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view. (Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the . **NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


