---
title: Filtre y enumere de forma eficaz elementos de una carpeta
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35215c24a9b953bf8406b268a6169abbd536202b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320310"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a>Filtre y enumere de forma eficaz elementos de una carpeta

En este ejemplo se muestra cómo usar el objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) para filtrar elementos de la Bandeja de entrada que tienen datos adjuntos y enumerar dichos elementos de forma eficaz, mostrando las propiedades seleccionadas de cada elemento.

## <a name="example"></a>Ejemplo

El ejemplo de código especifica la propiedad **PR\_HASATTACH** con el espacio de nombres MAPI y usa la propiedad para crear el filtro inicial en el método [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) de la Bandeja de entrada. Un objeto **Table** para un tipo de elemento tiene columnas predeterminadas que representan determinadas propiedades de ese tipo de elemento. Para personalizar las columnas, este ejemplo llama primero al método [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) en la colección [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) de esa **Tabla**, y luego llama al método [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) en la colección **Columns** para añadir las propiedades **EntryID**, **Subject** y **ReceivedTime** mediante los nombres de propiedad integrados, con la columna **ReceivedTime** almacenando los valores en la representación local de fecha y hora. 

Después, el ejemplo llama al **Columns.Add** una vez más para añadir la propiedad **ReceiveTime** especificando su espacio de nombres MAPI para que esta columna almacene el valor como un valor de fecha y hora de Tiempo Universal Coordinado (UTC). Por último, el ejemplo enumera cada elemento de la tabla, mostrando el valor de cada una de las cuatro propiedades especificadas como las columnas de la tabla.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
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
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
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

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

