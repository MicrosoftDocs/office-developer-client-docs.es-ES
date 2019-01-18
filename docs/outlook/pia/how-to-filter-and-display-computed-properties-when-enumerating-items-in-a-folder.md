---
title: Filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 946858221b649cd6189ddf44680b316554cab5de
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723078"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="36ae3-102">Filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta</span><span class="sxs-lookup"><span data-stu-id="36ae3-102">Filter and display computed properties when enumerating items in a folder</span></span>

<span data-ttu-id="36ae3-103">En este ejemplo se muestra cómo filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="36ae3-103">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="36ae3-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36ae3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="36ae3-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="36ae3-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="36ae3-106">El objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa un conjunto de datos de elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) o [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="36ae3-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="36ae3-107">El objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) representa las filas de datos de un objeto **Table**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-107">The [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object represents rows of data in a **Table**.</span></span> <span data-ttu-id="36ae3-108">El objeto [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) representa las propiedades del objeto **Table**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-108">The [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) object represents properties of the **Table**.</span></span> <span data-ttu-id="36ae3-109">Puede agregar determinadas propiedades al objeto **Table** mediante el método [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) del objeto **Columns**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-109">You can add certain properties to the **Table** object by using the [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method of the **Columns** object.</span></span> <span data-ttu-id="36ae3-110">Puede filtrar determinadas propiedades mediante el método [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) del objeto **Table**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-110">You can filter certain properties by using the [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) method of the **Table** object.</span></span> <span data-ttu-id="36ae3-111">Sin embargo, algunas de las propiedades no pueden agregarse al objeto **Table** mediante **Columns.Add** ni pueden filtrarse mediante el método **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-111">However, some properties cannot be added to the **Table** object by using **Columns.Add**, nor can they be filtered by using the **Restrict** method.</span></span> <span data-ttu-id="36ae3-112">En la siguiente tabla se muestra si el objeto **Table** admite las propiedades al usar el método **Columns.Add** o el método **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-112">The following table describes whether properties are supported for the **Table** object when you use the **Columns.Add** or **Restrict** method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36ae3-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36ae3-113">Property</span></span></p></th>
<th><p><span data-ttu-id="36ae3-114">Para Columns.Add</span><span class="sxs-lookup"><span data-stu-id="36ae3-114">For Columns.Add</span></span></p></th>
<th><p><span data-ttu-id="36ae3-115">Para Restrict</span><span class="sxs-lookup"><span data-stu-id="36ae3-115">For Restrict</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-116">Propiedades binarias, como <b>EntryID</b>.</span><span class="sxs-lookup"><span data-stu-id="36ae3-116">Binary properties such as <b>EntryID</b>.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-117">Se admiten a través de las propiedades integradas o de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="36ae3-117">Supported via built-in or namespace property.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-p102">No se admiten, Outlook mostrará un error.</span><span class="sxs-lookup"><span data-stu-id="36ae3-p102">Not supported. Outlook will raise an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ae3-120">Propiedades de cuerpo, como <b>Body</b> y <b>HTMLBody</b>; y la representación del espacio de nombres de esas propiedades, como <b>PR_RTF_COMPRESSED</b>.</span><span class="sxs-lookup"><span data-stu-id="36ae3-120">Body properties, including <b>Body</b> and <b>HTMLBody</b>, and namespace representation of those properties, including <b>PR_RTF_COMPRESSED</b>.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-121">La propiedad <b>Body</b> se admite con la condición de que solo los primeros 255 bytes del valor se almacenan en un objeto <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="36ae3-121">The <b>Body</b> property is supported with a condition that only the first 255 bytes of the value are stored in a <b>Table</b> object.</span></span> <span data-ttu-id="36ae3-122">No se admiten otras propiedades que representan el contenido del cuerpo en HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="36ae3-122">Other properties that represent the body content in HTML or RTF are not supported.</span></span> <span data-ttu-id="36ae3-123">Como solo se devuelven los primeros 255 bytes de la propiedad <b>Body</b>, si desea obtener todo el contenido del cuerpo de un elemento en texto o en HTML, use la propiedad <b>EntryID</b> del elemento en el método <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> para obtener el objeto de elemento.</span><span class="sxs-lookup"><span data-stu-id="36ae3-123">Because only the first 255 bytes of <b>Body</b> are returned, if you want to obtain the full body content of an item in text or HTML, use the item’s <b>EntryID</b> in the <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> method to obtain the item object.</span></span> <span data-ttu-id="36ae3-124">Después, recupere el valor completo de <b>Body</b> a través del objeto de elemento.</span><span class="sxs-lookup"><span data-stu-id="36ae3-124">Then retrieve the full value of <b>Body</b> through the item object.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-p104">En un filtro, solo se admite la propiedad <b>Body</b> representada en texto. Esto significa que se debe hacer referencia a la propiedad en un filtro de búsqueda y ubicación DAV (DASL) como <em>urn:schemas:http-mail:textdescription</em> y no puede filtrar por ninguna etiqueta HTML en el cuerpo. Para mejorar el rendimiento, utilice palabras clave de indizador de contexto en el filtro para que coincidan con cadenas en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="36ae3-p104">Only the <b>Body</b> property represented in text is supported in a filter. This means that the property must be referenced in a DAV Searching and Locating (DASL) filter as <em>urn:schemas:http-mail:textdescription</em>, and you cannot filter on any HTML tags in the body. To improve performance, use context indexer keywords in the filter to match strings in the body.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-128">Propiedades del equipo, como <b>AutoResolvedWinner</b> y <b>BodyFormat</b>.</span><span class="sxs-lookup"><span data-stu-id="36ae3-128">Computer properties, such as <b>AutoResolvedWinner</b> and <b>BodyFormat</b>.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-129">No admitidas.</span><span class="sxs-lookup"><span data-stu-id="36ae3-129">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-130">No admitidas.</span><span class="sxs-lookup"><span data-stu-id="36ae3-130">Not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ae3-131">Propiedades multivalor, como <b>Categories</b>, <b>Children</b>, <b>Companies</b> y <b>VotingOptions</b>.</span><span class="sxs-lookup"><span data-stu-id="36ae3-131">Multivalued properties, such as <b>Categories</b>, <b>Children</b>, <b>Companies</b>, and <b>VotingOptions</b>.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-132">Admitidas.</span><span class="sxs-lookup"><span data-stu-id="36ae3-132">Supported.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-133">Admitidas, siempre que se cree una consulta DASL mediante la representación del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="36ae3-133">Supported, provided that you can create a DASL query by using the namespace representation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-134">Propiedades que devuelven un objeto, como <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> y <b>UserProperties</b>.</span><span class="sxs-lookup"><span data-stu-id="36ae3-134">Properties that return an object, such as <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, and <b>UserProperties</b>.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-135">No admitidas.</span><span class="sxs-lookup"><span data-stu-id="36ae3-135">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="36ae3-136">No admitidas.</span><span class="sxs-lookup"><span data-stu-id="36ae3-136">Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36ae3-p105">En la tabla siguiente se enumeran las propiedades no válidas conocidas que no se pueden agregar al objeto **Table** mediante el uso de **Columns.Add**. Si intenta agregar una propiedad de esta lista, Outlook producirá un error.</span><span class="sxs-lookup"><span data-stu-id="36ae3-p105">The following table lists known invalid properties that cannot be added to the **Table** object by using **Columns.Add**. If you attempt to add a property from this list, Outlook will raise an error.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-139">AutoResolvedWinner</span><span class="sxs-lookup"><span data-stu-id="36ae3-139">AutoResolvedWinner</span></span></p></td>
<td><p><span data-ttu-id="36ae3-140">BodyFormat</span><span class="sxs-lookup"><span data-stu-id="36ae3-140">BodyFormat</span></span></p></td>
<td><p><span data-ttu-id="36ae3-141">Clase</span><span class="sxs-lookup"><span data-stu-id="36ae3-141">Class</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ae3-142">Companies</span><span class="sxs-lookup"><span data-stu-id="36ae3-142">Companies</span></span></p></td>
<td><p><span data-ttu-id="36ae3-143">ContactNames</span><span class="sxs-lookup"><span data-stu-id="36ae3-143">ContactNames</span></span></p></td>
<td><p><span data-ttu-id="36ae3-144">DLName</span><span class="sxs-lookup"><span data-stu-id="36ae3-144">DLName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-145">DownloadState</span><span class="sxs-lookup"><span data-stu-id="36ae3-145">DownloadState</span></span></p></td>
<td><p><span data-ttu-id="36ae3-146">FlagIcon</span><span class="sxs-lookup"><span data-stu-id="36ae3-146">FlagIcon</span></span></p></td>
<td><p><span data-ttu-id="36ae3-147">HtmlBody</span><span class="sxs-lookup"><span data-stu-id="36ae3-147">HtmlBody</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ae3-148">InternetCodePage</span><span class="sxs-lookup"><span data-stu-id="36ae3-148">InternetCodePage</span></span></p></td>
<td><p><span data-ttu-id="36ae3-149">IsConflict</span><span class="sxs-lookup"><span data-stu-id="36ae3-149">IsConflict</span></span></p></td>
<td><p><span data-ttu-id="36ae3-150">IsMarkedAsTask</span><span class="sxs-lookup"><span data-stu-id="36ae3-150">IsMarkedAsTask</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-151">MeetingWorkspaceURL</span><span class="sxs-lookup"><span data-stu-id="36ae3-151">MeetingWorkspaceURL</span></span></p></td>
<td><p><span data-ttu-id="36ae3-152">MemberCount</span><span class="sxs-lookup"><span data-stu-id="36ae3-152">MemberCount</span></span></p></td>
<td><p><span data-ttu-id="36ae3-153">Permission</span><span class="sxs-lookup"><span data-stu-id="36ae3-153">Permission</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ae3-154">PermissionService</span><span class="sxs-lookup"><span data-stu-id="36ae3-154">PermissionService</span></span></p></td>
<td><p><span data-ttu-id="36ae3-155">RecurrenceState</span><span class="sxs-lookup"><span data-stu-id="36ae3-155">RecurrenceState</span></span></p></td>
<td><p><span data-ttu-id="36ae3-156">ResponseState</span><span class="sxs-lookup"><span data-stu-id="36ae3-156">ResponseState</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ae3-157">Saved</span><span class="sxs-lookup"><span data-stu-id="36ae3-157">Saved</span></span></p></td>
<td><p><span data-ttu-id="36ae3-158">Enviados</span><span class="sxs-lookup"><span data-stu-id="36ae3-158">Sent</span></span></p></td>
<td><p><span data-ttu-id="36ae3-159">Enviado</span><span class="sxs-lookup"><span data-stu-id="36ae3-159">Submitted</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ae3-160">TaskSubject</span><span class="sxs-lookup"><span data-stu-id="36ae3-160">TaskSubject</span></span></p></td>
<td><p><span data-ttu-id="36ae3-161">No leídos</span><span class="sxs-lookup"><span data-stu-id="36ae3-161">Unread</span></span></p></td>
<td><p><span data-ttu-id="36ae3-162">VotingOptions</span><span class="sxs-lookup"><span data-stu-id="36ae3-162">VotingOptions</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36ae3-163">Aunque algunas propiedades calculadas no se pueden agregar a las columnas de una tabla, el siguiente ejemplo de código resuelve esta limitación.</span><span class="sxs-lookup"><span data-stu-id="36ae3-163">Although some computed properties cannot be added to the column set for a table, the following code example works around this limitation.</span></span> <span data-ttu-id="36ae3-164">GetToDoItems usa una consulta DASL para restringir los elementos que aparecen en el objeto **Table**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-164">GetToDoItems uses a DASL query to restrict the items that appear in the **Table**.</span></span> <span data-ttu-id="36ae3-165">Si la propiedad calculada tiene una representación del espacio de nombres, se usa la representación del espacio de nombres para crear una consulta DASL que restringe el objeto **Table** para que devuelva filas para un valor específico de la propiedad calculada.</span><span class="sxs-lookup"><span data-stu-id="36ae3-165">If the computed property has a namespace representation, the namespace representation is used to create a DASL query that restricts the **Table** object to return rows for a specified value of the computed property.</span></span> <span data-ttu-id="36ae3-166">GetToDoItems obtiene elementos de la Bandeja de entrada para los que el valor de la propiedad [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) es igual a **true**, y luego asigna valores a determinadas propiedades de las tareas, como [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) y [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="36ae3-166">GetToDoItems gets items in the Inbox where the value of the [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) property is equal to **true**, and then assigns values to certain task properties such as [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)), and [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span></span> <span data-ttu-id="36ae3-167">Por último, esas propiedades se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="36ae3-167">Finally, those properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="36ae3-168">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="36ae3-168">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="36ae3-169">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="36ae3-169">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="36ae3-170">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="36ae3-170">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "https://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "https://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="36ae3-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="36ae3-171">See also</span></span>

- [<span data-ttu-id="36ae3-172">Buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="36ae3-172">Search and filter</span></span>](search-and-filter.md)

