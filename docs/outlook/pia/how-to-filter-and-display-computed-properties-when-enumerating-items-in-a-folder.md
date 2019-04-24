---
title: Filtrar y mostrar propiedades calculadas al enumerar elementos de una carpeta
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 946858221b649cd6189ddf44680b316554cab5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320338"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a>Filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta

En este ejemplo se muestra cómo filtrar y mostrar propiedades calculadas al enumerar elementos en una carpeta.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


El objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa un conjunto de datos de elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) o [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). El objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) representa las filas de datos de un objeto **Table**. El objeto [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) representa las propiedades del objeto **Table**. Puede agregar determinadas propiedades al objeto **Table** mediante el método [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) del objeto **Columns**. Puede filtrar determinadas propiedades mediante el método [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) del objeto **Table**. Sin embargo, algunas de las propiedades no pueden agregarse al objeto **Table** mediante **Columns.Add** ni pueden filtrarse mediante el método **Restrict**. En la siguiente tabla se muestra si el objeto **Table** admite las propiedades al usar el método **Columns.Add** o el método **Restrict**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propiedad</p></th>
<th><p>Para Columns.Add</p></th>
<th><p>Para Restrict</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Propiedades binarias, como <b>EntryID</b>.</p></td>
<td><p>Se admiten a través de las propiedades integradas o de espacio de nombres.</p></td>
<td><p>No se admiten, Outlook mostrará un error.</p></td>
</tr>
<tr class="even">
<td><p>Propiedades de cuerpo, como <b>Body</b> y <b>HTMLBody</b>; y la representación del espacio de nombres de esas propiedades, como <b>PR_RTF_COMPRESSED</b>.</p></td>
<td><p>La propiedad <b>Body</b> se admite con la condición de que solo los primeros 255 bytes del valor se almacenan en un objeto <b>Table</b>. No se admiten otras propiedades que representan el contenido del cuerpo en HTML o RTF. Como solo se devuelven los primeros 255 bytes de la propiedad <b>Body</b>, si desea obtener todo el contenido del cuerpo de un elemento en texto o en HTML, use la propiedad <b>EntryID</b> del elemento en el método <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> para obtener el objeto de elemento. Después, recupere el valor completo de <b>Body</b> a través del objeto de elemento.</p></td>
<td><p>En un filtro, solo se admite la propiedad <b>Body</b> representada en texto. Esto significa que se debe hacer referencia a la propiedad en un filtro de búsqueda y ubicación DAV (DASL) como <em>urn:schemas:http-mail:textdescription</em> y no puede filtrar por ninguna etiqueta HTML en el cuerpo. Para mejorar el rendimiento, utilice palabras clave de indizador de contexto en el filtro para que coincidan con cadenas en el cuerpo.</p></td>
</tr>
<tr class="odd">
<td><p>Propiedades del equipo, como <b>AutoResolvedWinner</b> y <b>BodyFormat</b>.</p></td>
<td><p>No se admite.</p></td>
<td><p>No se admite.</p></td>
</tr>
<tr class="even">
<td><p>Propiedades multivalor, como <b>Categories</b>, <b>Children</b>, <b>Companies</b> y <b>VotingOptions</b>.</p></td>
<td><p>Admitidas.</p></td>
<td><p>Admitidas, siempre que se cree una consulta DASL mediante la representación del espacio de nombres.</p></td>
</tr>
<tr class="odd">
<td><p>Propiedades que devuelven un objeto, como <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> y <b>UserProperties</b>.</p></td>
<td><p>No se admite.</p></td>
<td><p>No se admite.</p></td>
</tr>
</tbody>
</table>


En la tabla siguiente se enumeran las propiedades no válidas conocidas que no se pueden agregar al objeto **Table** mediante el uso de **Columns.Add**. Si intenta agregar una propiedad de esta lista, Outlook producirá un error.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>AutoResolvedWinner</p></td>
<td><p>BodyFormat</p></td>
<td><p>Clase</p></td>
</tr>
<tr class="even">
<td><p>Companies</p></td>
<td><p>ContactNames</p></td>
<td><p>DLName</p></td>
</tr>
<tr class="odd">
<td><p>DownloadState</p></td>
<td><p>FlagIcon</p></td>
<td><p>HtmlBody</p></td>
</tr>
<tr class="even">
<td><p>InternetCodePage</p></td>
<td><p>IsConflict</p></td>
<td><p>IsMarkedAsTask</p></td>
</tr>
<tr class="odd">
<td><p>MeetingWorkspaceURL</p></td>
<td><p>MemberCount</p></td>
<td><p>Permission</p></td>
</tr>
<tr class="even">
<td><p>PermissionService</p></td>
<td><p>RecurrenceState</p></td>
<td><p>ResponseState</p></td>
</tr>
<tr class="odd">
<td><p>Saved</p></td>
<td><p>Enviados</p></td>
<td><p>Enviado</p></td>
</tr>
<tr class="even">
<td><p>TaskSubject</p></td>
<td><p>No leídos</p></td>
<td><p>VotingOptions</p></td>
</tr>
</tbody>
</table>


Aunque algunas propiedades calculadas no se pueden agregar a las columnas de una tabla, el siguiente ejemplo de código resuelve esta limitación. GetToDoItems usa una consulta DASL para restringir los elementos que aparecen en el objeto **Table**. Si la propiedad calculada tiene una representación del espacio de nombres, se usa la representación del espacio de nombres para crear una consulta DASL que restringe el objeto **Table** para que devuelva filas para un valor específico de la propiedad calculada. GetToDoItems obtiene elementos de la Bandeja de entrada para los que el valor de la propiedad [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) es igual a **true**, y luego asigna valores a determinadas propiedades de las tareas, como [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) y [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)). Por último, esas propiedades se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

