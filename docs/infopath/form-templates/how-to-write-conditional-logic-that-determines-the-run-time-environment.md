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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299730"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Escribir lógica condicional que deTermine el entorno en tiempo de ejecución

La propiedad [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtiene una referencia a un objeto [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , que se puede usar para determinar el entorno en tiempo de ejecución (InfoPath, explorador web o explorador móvil) que se utilizó para abrir el formulario. 
  
## <a name="example"></a>Ejemplo

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Determinar el entorno en tiempo de ejecución en el que se ejecuta un formulario

La clase [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) proporciona las propiedades [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) y [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , que le permiten determinar el entorno de edición que se utilizó para abrir una plantilla de formulario. Si las dos propiedades devuelven **false**, la plantilla se abrió en el editor de Microsoft InfoPath. Si una de las propiedades devuelve **true**, se abrió desde una biblioteca de documentos configurada adecuadamente en Microsoft SharePoint Server 2010 con InfoPath Forms Services en el programa correspondiente a la propiedad: un explorador web (propiedad [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ) o un explorador móvil (propiedad [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ). 
  
En el ejemplo siguiente, si el formulario se abre en un explorador o en un explorador móvil, el valor del campo1 (que está enlazado a un control **Cuadro de texto**) se establece como una cadena para indicar el entorno en tiempo de ejecución en que se abrió el formulario. Si el formulario se abrió en InfoPath, el método **System.Windows.Forms.MessageBox.Show** (que no está disponible cuando un formulario se ejecuta en un explorador) se utiliza para mostrar un cuadro de mensaje. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Cuando se crea una plantilla de formulario para el siguiente ejemplo de código, seleccione la plantilla **En blanco** de la ficha **Nuevo** en la vista Backstage. (También puede seleccionar **Formulario de explorador web** de la lista desplegable **Tipo de formulario** bajo la categoría **Compatibilidad** del cuadro de diálogo **Opciones de formulario**). Para que se admita la clase **MessageBox**, agregue una referencia a **System.Windows.Forms** en la ficha **NET** del cuadro de diálogo **Agregar referencia** en Visual Studio 2012 y, después, agregue una directiva **using** o **Imports** para **System.Windows.Forms** en la sección de declaraciones del módulo de código del formulario. 
  
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


