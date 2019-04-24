---
title: Configurar el ámbito de variables correctamente en controladores de eventos
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8a1a418a315167cc96be5b9b5f65a0f4cd9ce44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342255"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a>Configurar el ámbito de variables correctamente en controladores de eventos

Un error frecuente en la programación de controladores de eventos es conectar el controlador de eventos a un objeto que se ha declarado con un ámbito demasiado limitado para el objetivo de controlar el evento. El objeto debe tener una duración que no sólo abarque la función que conecta el método de devolución de llamada como controlador de eventos del objeto, sino también el método de devolución de llamada en sí donde se controla en realidad el evento. De lo contrario, si el objeto está fuera de ámbito y ya no se define en el método de devolución de llamada, ya no se llama al método de devolución de llamada y el evento no se controla según lo deseado. 

En el ejemplo siguiente se intenta conectar el método de devolución de llamada MyNewInspector al evento [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)). Sin embargo, el método de devolución de llamada se enlaza en el ejemplo de código al evento NewInspector de un objeto [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) que tiene un ámbito limitado a la función Connect. Cuando finalmente se llama al método de devolución de llamada, la función Connect ya se ha completado, el objeto Inspectors ya ha sido recolectado como elemento no utilizado y, por tanto, nunca se llama al MyNewInspector.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyApp.Inspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

Lo que debe hacer en este caso es almacenar el objeto Inspectors en una variable más permanente con una duración que abarque todo MyClass, incluso el método de devolución de llamada MyNewInspector. En el siguiente ejemplo, MyInspectors tiene un ámbito de todo MyClass y garantiza que el método de devolución de llamada se conecta por la duración de la clase.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;
    private Outlook.Inspectors MyInspectors;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyInspectors = MyApp.Inspectors;
        MyInspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

En función de las diferencias sintácticas con las que los distintos lenguajes conectan los controladores de eventos, este problema es menos frecuente en lenguajes como Visual Basic, donde puede conectar un evento especificando una instancia del objeto primario y definir el método de devolución de llamada en el mismo momento. En el siguiente ejemplo de Visual Basic, se usa la palabra clave Handles para conectar el método de devolución de llamada Region\_Expanded al evento [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)). Una instancia del objeto primario, Region, tiene un ámbito que abarca MyClass, incluido el método de devolución de llamada Region\_Expanded.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Public Class MyClass
    ' The Region object has a lifetime spanning the class 
    ' including the callback method Region_Expanded
    Private WithEvents Region As Outlook.FormRegion
    ...
    Private Sub Region_Expanded() Handles Region.Expanded
        MsgBox("My EventHandler caught an Expanded event.")
    End Sub
End Class
```

En este ejemplo, dado que el método de devolución de Region\_Expanded se conecta al evento Expanded por la duración de la clase, se llama al método de devolución de llamada según corresponda.

## <a name="see-also"></a>Vea también

- [Conexión con controladores de eventos personalizados](connecting-to-custom-event-handlers.md)

