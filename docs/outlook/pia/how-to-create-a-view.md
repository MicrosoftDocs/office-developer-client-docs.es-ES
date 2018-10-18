---
title: Crear una vista
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e9a68fc6220e1439e517b3d4e7e2ecb30b919ee0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406032"
---
# <a name="create-a-view"></a><span data-ttu-id="67f47-102">Crear una vista</span><span class="sxs-lookup"><span data-stu-id="67f47-102">Create a map view programmatically</span></span>

<span data-ttu-id="67f47-103">En este ejemplo se usa el método [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) de la colección [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) para crear una vista para un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="67f47-103">This example shows how to use the [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) method of the [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) collection to create a view for a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="67f47-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67f47-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="67f47-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="67f47-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="67f47-p101">Puede crear vistas personalizables que permitan ordenar, agrupar y ver datos de todos los tipos diferentes dentro del panel de vista de la ventana del explorador de Outlook. También puede personalizar vistas integradas mediante programación. En la tabla siguiente se enumeran objetos que representan vistas de Outlook. </span><span class="sxs-lookup"><span data-stu-id="67f47-p101">You can create customizable views that allow you to sort, group, and view data of all different types within the View Pane of the Outlook explorer window. You can also customize built-in views programmatically. The following table lists objects that represent Outlook views.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67f47-109">Nombre de objeto</span><span class="sxs-lookup"><span data-stu-id="67f47-109">Object Name</span></span></p></th>
<th><p><span data-ttu-id="67f47-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f47-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67f47-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span><span class="sxs-lookup"><span data-stu-id="67f47-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="67f47-112">Los datos se ven como una serie de imágenes de tarjeta de presentación electrónica.</span><span class="sxs-lookup"><span data-stu-id="67f47-112">Data is viewed as a series of Electronic Business Card images.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f47-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span><span class="sxs-lookup"><span data-stu-id="67f47-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span></span></p></td>
<td><p><span data-ttu-id="67f47-114">Los datos se ven en un formato de calendario.</span><span class="sxs-lookup"><span data-stu-id="67f47-114">Data is viewed in a calendar format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f47-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span><span class="sxs-lookup"><span data-stu-id="67f47-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="67f47-116">Los datos se ven en una serie de tarjetas.</span><span class="sxs-lookup"><span data-stu-id="67f47-116">Data is viewed in a series of cards.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f47-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span><span class="sxs-lookup"><span data-stu-id="67f47-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView Object</a></span></span></p></td>
<td><p><span data-ttu-id="67f47-118">Los datos se ven como iconos de explorador o iconos de carpeta de Windows.</span><span class="sxs-lookup"><span data-stu-id="67f47-118">Data is viewed as Windows folder icons or explorer icons.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f47-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span><span class="sxs-lookup"><span data-stu-id="67f47-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView Object</a></span></span></p></td>
<td><p><span data-ttu-id="67f47-120">Los datos se ven en una tabla sencilla basada en campos.</span><span class="sxs-lookup"><span data-stu-id="67f47-120">Data is viewed in a simple field-based table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f47-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span><span class="sxs-lookup"><span data-stu-id="67f47-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView Object</a></span></span></p></td>
<td><p><span data-ttu-id="67f47-122">Los datos se ven en una línea de tiempo lineal personalizable.</span><span class="sxs-lookup"><span data-stu-id="67f47-122">Data is viewed in a customizable linear time line.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67f47-123">Puede acceder a las propiedades y los métodos comunes para todas las vistas mediante el objeto [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="67f47-123">You can access properties and methods that are common to all views by using the [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) object.</span></span> <span data-ttu-id="67f47-124">Sin embargo, para obtener acceso a algunas propiedades que no son comunes para todas las vistas, debe convertir el objeto **View** en un objeto **View** derivado al que pertenezca la propiedad a la que quiera obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="67f47-124">However, to access certain properties that are not common to all views, you must cast the **View** object to a derived **View** object that the property you want to access belongs to.</span></span> <span data-ttu-id="67f47-125">Por ejemplo, para obtener acceso a la propiedad [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) del objeto **Cardview**, debe convertir el objeto **View** en un objeto **Cardview**.</span><span class="sxs-lookup"><span data-stu-id="67f47-125">For example, to access the [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) property of the **Cardview** object, cast the **View** object to the **Cardview** object.</span></span> <span data-ttu-id="67f47-126">Si quiere determinar qué tipo de vista se representa con un determinado objeto **View**, use la propiedad [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="67f47-126">If you want to determine which type of view is represented by a particular **View** object, use the [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) property.</span></span>

<span data-ttu-id="67f47-127">Para crear una nueva vista, use el método **Add** de la colección **Views** para un objeto **Folder**.</span><span class="sxs-lookup"><span data-stu-id="67f47-127">To create a new view, use the **Add** method of the **Views** collection for a **Folder** object.</span></span> <span data-ttu-id="67f47-128">Después, establezca la visibilidad de la vista en el momento de la creación o en cualquier momento después de crear la vista.</span><span class="sxs-lookup"><span data-stu-id="67f47-128">Then set the visibility for the view either at the time of creation, or at any time after the view is created.</span></span> <span data-ttu-id="67f47-129">Para establecer la visibilidad de la vista en el momento de creación, especifique una constante [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) en el parámetro *SaveOption* del método **Add**.</span><span class="sxs-lookup"><span data-stu-id="67f47-129">To set the visibility for the view at the time of creation, specify an [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) constant in the *SaveOption* parameter of the **Add** method.</span></span> <span data-ttu-id="67f47-130">Para establecer la visibilidad en cualquier momento después de la creación de la vista, especifique una constante **OlViewSaveOption** para la propiedad [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) del objeto **View**.</span><span class="sxs-lookup"><span data-stu-id="67f47-130">To set the visibility at any time after the view is created, specify an **OlViewSaveOption** constant for the [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) property of the **View** object.</span></span> 

<span data-ttu-id="67f47-131">Agregar una nueva vista genera el evento [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) de la colección **Views**.</span><span class="sxs-lookup"><span data-stu-id="67f47-131">Adding a new view raises the  ViewAdd  event of the Views collection.You can use the  Remove  method of the Views object to remove an existing custom view.</span></span> <span data-ttu-id="67f47-132">Una vez que se crea la vista, puede personalizarla mediante programación convirtiendo el objeto **View** en uno de los objetos derivados y, después, haciendo los cambios necesarios.</span><span class="sxs-lookup"><span data-stu-id="67f47-132">Once the view is created, customize the view programmatically by casting the **View** object to one of the derived objects and then making necessary changes.</span></span> <span data-ttu-id="67f47-133">Use el método **Save** del objeto **View** derivado del objeto **View** para guardar los cambios realizados en la vista.</span><span class="sxs-lookup"><span data-stu-id="67f47-133">Use the **Save** method of the derived **View** object or the **View** object to save any changes to the view.</span></span> <span data-ttu-id="67f47-134">Por último, use el método **Apply** del objeto **View**derivado del objeto **View** para aplicar la vista al objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) actual.</span><span class="sxs-lookup"><span data-stu-id="67f47-134">Finally, use the **Apply** method of the derived **View** object or the **View** object to apply the view to the current [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="67f47-135">Esto genera el evento [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) del objeto **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="67f47-135">Applying a view raises the [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) event of the **Explorer** object.</span></span>

<span data-ttu-id="67f47-136">En el ejemplo de código siguiente, CreateMeetingRequestsView agrega una nueva vista denominada "Meeting Requests" a la Bandeja de entrada del usuario convirtiendo el objeto **View** en un objeto **TableView**.</span><span class="sxs-lookup"><span data-stu-id="67f47-136">In the following code example, CreateMeetingRequestsView adds a new view named “Meeting Requests” to the user’s Inbox by casting the **View** object to a **TableView** object.</span></span> <span data-ttu-id="67f47-137">Después, CreateMeetingRequestsView llama al método **Add** del objeto **Views** con el parámetro *Name* establecido en “Meeting Requests” y el parámetro *ViewType* establecido en **olTableView**.</span><span class="sxs-lookup"><span data-stu-id="67f47-137">CreateMeetingRequestsView then calls the **Add** method of the **Views** object with the *Name* parameter set to “Meeting Requests” and the *ViewType* parameter set to **olTableView**.</span></span> <span data-ttu-id="67f47-138">La propiedad [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) del objeto **TableView** se establece en una cadena de búsqueda y ubicación DAV (DASL) que hace que la vista se muestre únicamente cuando hay elementos que contienen "IPM.Schedule" en la clase de mensaje para el elemento.</span><span class="sxs-lookup"><span data-stu-id="67f47-138">The [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) property of the **TableView** object is set to a DAV Searching and Locating (DASL) string that causes the view to display only when there are items that contain “IPM.Schedule” in the message class for the item.</span></span> <span data-ttu-id="67f47-139">Después, se guarda y se aplica la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="67f47-139">The new view is then saved and applied.</span></span>

<span data-ttu-id="67f47-140">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="67f47-140">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="67f47-141">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="67f47-141">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="67f47-142">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="67f47-142">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a><span data-ttu-id="67f47-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="67f47-143">See also</span></span>

- [<span data-ttu-id="67f47-144">Vistas</span><span class="sxs-lookup"><span data-stu-id="67f47-144">Views</span></span>](views.md)

