---
title: Configurar el ámbito de variables correctamente en controladores de eventos
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ac26dfb245dd9b4621093a91ff36846c686f6e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407607"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a><span data-ttu-id="ef4d7-102">Configurar el ámbito de variables correctamente en controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="ef4d7-102">Scoping Variables Appropriately in Event Handlers</span></span>

<span data-ttu-id="ef4d7-p101">Un error frecuente en la programación de controladores de eventos es conectar el controlador de eventos a un objeto que se ha declarado con un ámbito demasiado limitado para el objetivo de controlar el evento. El objeto debe tener una duración que no sólo abarque la función que conecta el método de devolución de llamada como controlador de eventos del objeto, sino también el método de devolución de llamada en sí donde se controla en realidad el evento. De lo contrario, si el objeto está fuera de ámbito y ya no se define en el método de devolución de llamada, ya no se llama al método de devolución de llamada y el evento no se controla según lo deseado. </span><span class="sxs-lookup"><span data-stu-id="ef4d7-p101">A common mistake in programming event handlers is connecting the event handler to an object that has been declared with a scope too limited for the purpose of handling the event. The object must have a life that spans not just over the function that connects the callback method as an event handler of the object, but also over the callback method itself where the event is actually handled. Otherwise, if the object is out of scope and is no longer defined in the callback method, the callback method is not called and the event is not handled as desired.</span></span>

<span data-ttu-id="ef4d7-106">En el ejemplo siguiente se intenta conectar el método de devolución de llamada MyNewInspector al evento [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ef4d7-106">The following example attempts to connect the MyNewInspector callback method to the [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) event.</span></span> <span data-ttu-id="ef4d7-107">Sin embargo, el método de devolución de llamada se enlaza en el ejemplo de código al evento NewInspector de un objeto [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) que tiene un ámbito limitado a la función Connect.</span><span class="sxs-lookup"><span data-stu-id="ef4d7-107">However, the callback method is hooked up in the code sample to the NewInspector event of an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) object that has a scope limited to the Connect function.</span></span> <span data-ttu-id="ef4d7-108">Cuando finalmente se llama al método de devolución de llamada, la función Connect ya se ha completado, el objeto Inspectors ya ha sido recolectado como elemento no utilizado y, por tanto, nunca se llama al MyNewInspector.</span><span class="sxs-lookup"><span data-stu-id="ef4d7-108">When the callback method is eventually called, the Connect function has already exited, the Inspectors object has already been garbage collected, and so MyNewInspector is never called.</span></span>

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

<span data-ttu-id="ef4d7-p103">Lo que debe hacer en este caso es almacenar el objeto Inspectors en una variable más permanente con una duración que abarque todo MyClass, incluso el método de devolución de llamada MyNewInspector. En el siguiente ejemplo, MyInspectors tiene un ámbito de todo MyClass y garantiza que el método de devolución de llamada se conecta por la duración de la clase.</span><span class="sxs-lookup"><span data-stu-id="ef4d7-p103">The correct thing to do in this case is to store the Inspectors object in a more permanent variable whose lifetime spans over the entire MyClass, including the MyNewInspector callback method. In the following example, MyInspectors has a scope of the entire MyClass and ensures that the callback method is connected for the lifetime of the class.</span></span>

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

<span data-ttu-id="ef4d7-111">En función de las diferencias sintácticas con las que los distintos lenguajes conectan los controladores de eventos, este problema es menos frecuente en lenguajes como Visual Basic, donde puede conectar un evento especificando una instancia del objeto primario y definir el método de devolución de llamada en el mismo momento.</span><span class="sxs-lookup"><span data-stu-id="ef4d7-111">By virtue of the syntactic differences in how various languages connect event handlers, this issue is less common in languages such as Visual Basic where you can connect an event specifying an instance of the parent object, and define the callback method at the same time. The following example in Visual Basic uses the Handles keyword to connect the Region_Expanded callback method to the E:Microsoft.Office.Interop.Outlook.FormRegionEvents_Event.Expanded event. An instance of the parent object, Region, has a scope that spans MyClass including the Region_Expanded callback method.</span></span> <span data-ttu-id="ef4d7-112">En el siguiente ejemplo de Visual Basic, se usa la palabra clave Handles para conectar el método de devolución de llamada Region\_Expanded al evento [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ef4d7-112">The following example in Visual Basic uses the Handles keyword to connect the Region\_Expanded callback method to the [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) event.</span></span> <span data-ttu-id="ef4d7-113">Una instancia del objeto primario, Region, tiene un ámbito que abarca MyClass, incluido el método de devolución de llamada Region\_Expanded.</span><span class="sxs-lookup"><span data-stu-id="ef4d7-113">An instance of the parent object, Region, has a scope that spans MyClass including the Region\_Expanded callback method.</span></span>

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

<span data-ttu-id="ef4d7-114">En este ejemplo, dado que el método de devolución de Region\_Expanded se conecta al evento Expanded por la duración de la clase, se llama al método de devolución de llamada según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ef4d7-114">In this example, because the Region_Expanded callback method is connected to the Expanded event for the lifetime of the class, the callback method is called as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef4d7-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef4d7-115">See also</span></span>

- [<span data-ttu-id="ef4d7-116">Conexión con controladores de eventos personalizados</span><span class="sxs-lookup"><span data-stu-id="ef4d7-116">Connecting to Custom Event Handlers</span></span>](connecting-to-custom-event-handlers.md)

