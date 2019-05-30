---
title: Filtre y enumere de forma eficaz elementos de una carpeta
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1d5b293f89c453886cafd9effc3fb5205f9696c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542600"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="dde07-102">Filtre y enumere de forma eficaz elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="dde07-102">Filter and efficiently enumerate items in a folder</span></span>

<span data-ttu-id="dde07-103">En este ejemplo se muestra cómo usar el objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) para filtrar elementos de la Bandeja de entrada que tienen datos adjuntos y enumerar dichos elementos de forma eficaz, mostrando las propiedades seleccionadas de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="dde07-103">This example shows how to use the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to filter for items in the Inbox that have attachments, and efficiently enumerate such items, displaying selected properties for each item.</span></span>

## <a name="example"></a><span data-ttu-id="dde07-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dde07-104">Example</span></span>

<span data-ttu-id="dde07-105">El ejemplo de código especifica la propiedad **PR\_HASATTACH** con el espacio de nombres MAPI y usa la propiedad para crear el filtro inicial en el método [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="dde07-105">The code sample specifies the property **PR\_HASATTACH** with the MAPI namespace, and uses the property to create the initial filter in the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox.</span></span> <span data-ttu-id="dde07-106">Un objeto **Table** para un tipo de elemento tiene columnas predeterminadas que representan determinadas propiedades de ese tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="dde07-106">A **Table** object for an item type has default columns representing certain properties of that item type.</span></span> <span data-ttu-id="dde07-107">Para personalizar las columnas, este ejemplo llama primero al método [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) en la colección [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) de esa **Tabla**, y luego llama al método [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) en la colección **Columns** para añadir las propiedades **EntryID**, **Subject** y **ReceivedTime** mediante los nombres de propiedad integrados, con la columna **ReceivedTime** almacenando los valores en la representación local de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="dde07-107">To customize the columns, this example first calls the [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) method on the [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) collection of that **Table**, and then calls the [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method on the **Columns** collection to add the **EntryID**, **Subject**, and **ReceivedTime** properties using the built-in property names, with the **ReceivedTime** column storing values in local date-time representation.</span></span> 

<span data-ttu-id="dde07-108">Después, el ejemplo llama al **Columns.Add** una vez más para añadir la propiedad **ReceiveTime** especificando su espacio de nombres MAPI para que esta columna almacene el valor como un valor de fecha y hora de Tiempo Universal Coordinado (UTC).</span><span class="sxs-lookup"><span data-stu-id="dde07-108">The example then calls **Columns.Add** one more time to add the **ReceiveTime** property specifying its MAPI namespace so that this column will store the value as a Universal Coordinated Time (UTC) date-time value.</span></span> <span data-ttu-id="dde07-109">Por último, el ejemplo enumera cada elemento de la tabla, mostrando el valor de cada una de las cuatro propiedades especificadas como las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="dde07-109">Finally, the example enumerates each item in the Table, displaying the value of each of the four properties specified as the table columns.</span></span>

<span data-ttu-id="dde07-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dde07-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="dde07-111">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="dde07-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="dde07-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="dde07-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
    ' Obtain Inbox
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox), _
        Outlook.Folder)
    ' Create filter
    Dim filter As String = "@SQL=" & Chr(34) _
        & PR_HAS_ATTACH & Chr(34) & " = 1"
    Dim table As Outlook.Table = _
        folder.GetTable(filter, _
        Outlook.OlTableContents.olUserItems)
    ' Remove default columns
    table.Columns.RemoveAll()
    ' Add using built-in name
    table.Columns.Add("EntryID")
    table.Columns.Add("Subject")
    table.Columns.Add("ReceivedTime")
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending)
    ' Add using namespace
    ' Date received
    table.Columns.Add( _
        "urn:schemas:httpmail:datereceived")
    While Not (table.EndOfTable)
        Dim nextRow As Outlook.Row = table.GetNextRow()
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(nextRow("Subject").ToString())
        ' Reference column by name 
        sb.AppendLine("Received (Local): " _
            & nextRow("ReceivedTime").ToString())
        ' Reference column by index
        sb.AppendLine("Received (UTC): " & nextRow(4).ToString())
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    End While
End Sub
```


```csharp
private void DemoTableColumns()
{
    const string PR_HAS_ATTACH =
        "http://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Create filter
    string filter = "@SQL=" + "\""
        + PR_HAS_ATTACH + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Remove default columns
    table.Columns.RemoveAll();
    // Add using built-in name
    table.Columns.Add("EntryID");
    table.Columns.Add("Subject");
    table.Columns.Add("ReceivedTime");
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending);
    // Add using namespace
    // Date received
    table.Columns.Add(
        "urn:schemas:httpmail:datereceived");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(nextRow["Subject"].ToString());
        // Reference column by name 
        sb.AppendLine("Received (Local): "
            + nextRow["ReceivedTime"]);
        // Reference column by index
        sb.AppendLine("Received (UTC): " + nextRow[4]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dde07-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="dde07-113">See also</span></span>

- <span data-ttu-id="dde07-114">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="dde07-114">[Search and filter](search-and-filter.md)</span></span>

