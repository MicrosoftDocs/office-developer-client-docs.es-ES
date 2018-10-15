---
title: Agregar campos a una vista
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1ee143dfcd3ab3b3f2bfbbc82caf0558778a6cdc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406900"
---
# <a name="add-fields-to-a-view"></a><span data-ttu-id="b980d-102">Agregar campos a una vista</span><span class="sxs-lookup"><span data-stu-id="b980d-102">Add fields to a view</span></span>

<span data-ttu-id="b980d-103">En este ejemplo se muestra cómo personalizar una vista mediante el método [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) de la colección [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) para agregar campos a una vista.</span><span class="sxs-lookup"><span data-stu-id="b980d-103">This example shows how to customize a view by using the [M:Microsoft.Office.Interop.Outlook._ViewFields.Add(System.String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) method of the [T:Microsoft.Office.Interop.Outlook.ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) collection to add fields to a view.</span></span>

## <a name="example"></a><span data-ttu-id="b980d-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b980d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b980d-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b980d-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="b980d-106">Puede especificar qué propiedades de elemento de Outlook se muestran en una vista agregando una o más propiedades a la colección **ViewFields** solo para los objetos [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) y [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b980d-106">You can specify which Outlook item properties are displayed in a view by adding one or more properties to the  ViewFields  collection of any of the following objects:</span></span> <span data-ttu-id="b980d-107">Para otros objetos **View** derivados como [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) y [TimelineView ](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) use otros métodos para determinar qué propiedades del elemento de Outlook se muestran en la vista.</span><span class="sxs-lookup"><span data-stu-id="b980d-107">For other derived **View** objects such as [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)), and [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) objects, use other methods of determining which Outlook item properties are displayed within the view.</span></span> <span data-ttu-id="b980d-108">Por ejemplo, los campos que se muestran para el objeto **BusinessCardView** se determinan según el diseño de tarjeta de presentación electrónica (EBC) asociado a cada elemento de Outlook mostrado.</span><span class="sxs-lookup"><span data-stu-id="b980d-108">For example, the fields displayed for the **BusinessCardView** object are determined by the electronic business card (EBC) layout associated with each displayed Outlook item.</span></span>

<span data-ttu-id="b980d-109">Para obtener la colección **ViewFields** para una vista, use la propiedad **ViewFields** del objeto **View** asociado (por ejemplo, los objetos **CardView**o **TableView**).</span><span class="sxs-lookup"><span data-stu-id="b980d-109">To get the **ViewFields** collection for a view, use the **ViewFields** property of the associated **View** object (for example, the **CardView** or **TableView** objects).</span></span> <span data-ttu-id="b980d-110">El método **Add** de la colección **ViewFields** se utiliza para crear un objeto [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) que representa la propiedad del elemento de Outlook que se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="b980d-110">The ViewFields collection for those views can be retrieved by calling the ViewFields property of the appropriate view object. The  Add  method of the ViewFields collection is used to create a  ViewField  object that represents the Outlook item property to be displayed in the view.</span></span> <span data-ttu-id="b980d-111">Un objeto **ViewField** no solo identifica la propiedad de elemento de Outlook que se va a mostrar dentro de la vista, sino que también describe cómo se deben mostrar los valores de dicha propiedad.</span><span class="sxs-lookup"><span data-stu-id="b980d-111">A **ViewField** object not only identifies an Outlook item property to display within the view, but also describes how the values for that property should be displayed. You can change how properties are displayed in a view.</span></span> <span data-ttu-id="b980d-112">Puede cambiar cómo se muestran las propiedades de columna en una vista modificando la propiedad [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) del objeto **ViewField**.</span><span class="sxs-lookup"><span data-stu-id="b980d-112">You can change how individual column properties are displayed in a view by modifying the [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) property of the **ViewField** object.</span></span>

<span data-ttu-id="b980d-p103">En el ejemplo de código siguiente, ModifyMeetingRequestsView obtiene el objeto **TableView** que representa todas las vistas desde la Bandeja de entrada del usuario que son vistas de "Convocatorias de reunión". A continuación, en el ejemplo se usa el método **Add** para agregar los campos "Inicio" y "Fin" al objeto **ViewFields** corresponde al objeto **TableView**. También se cambia la etiqueta para el campo "De" a "Organizada por". A continuación, ModifyMeetingRequestsView, guarda el objeto **TableView** modificado.</span><span class="sxs-lookup"><span data-stu-id="b980d-p103">In the following code example, ModifyMeetingRequestsView gets the **TableView** object that represents all the views from the user’s Inbox that are “Meeting Requests” views. The example then uses the **Add** method to add the “Start” and “End” fields to the **ViewFields** object that corresponds to the **TableView** object. It also changes the label for the “From” field to “Organized By”. ModifyMeetingRequestsView then saves the modified **TableView** object.</span></span>

<span data-ttu-id="b980d-117">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b980d-117">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="b980d-118">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública.</span><span class="sxs-lookup"><span data-stu-id="b980d-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b980d-119">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="b980d-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b980d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b980d-120">See also</span></span>

- [<span data-ttu-id="b980d-121">Vistas</span><span class="sxs-lookup"><span data-stu-id="b980d-121">Views</span></span>](views.md)

