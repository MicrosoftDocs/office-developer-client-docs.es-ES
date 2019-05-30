---
title: Filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6242506bac081ee16d125ea92fbed69939c6abc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542628"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a>Filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta

En este ejemplo se muestra cómo filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

El objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa un conjunto de datos de elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) o [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Cuando se agrega por primera vez una propiedad binaria, de fecha o multivalor a un objeto **Table**, la manera en la que se hace referencia a la propiedad afecta a su tipo y a su formato. Como las referencias de nombres integrados devuelven a veces un valor de otra columna en lugar de una referencia de espacio de nombres, debe determinar si se hace referencia a la propiedad por su nombre explícito integrado (si procede) o por espacio de nombres (independientemente de la existencia de un nombre explícito integrado). En la tabla siguiente se muestran las diferencias entre las representaciones de los valores de las propiedades (según su tipo y formato) de acuerdo con el tipo original de la propiedad:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo</p></th>
<th><p>Tipo devuelto si la propiedad especificada usa un nombre integrado</p></th>
<th><p>Tipo devuelto si la propiedad especificada usa un espacio de nombres</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Binario (<b>PT_BINARY</b>)</p></td>
<td><p>Cadena</p></td>
<td><p>Matriz de bytes</p></td>
</tr>
<tr class="even">
<td><p>Fecha (<b>PT_SYSTIME</b>)</p></td>
<td><p><b>DateTime</b> local</p></td>
<td><p><b>DateTime</b> UTC</p></td>
</tr>
<tr class="odd">
<td><p>Multivalor (también conocido como tipo de palabra clave), como la propiedad <b>Categories</b> (<b>PT_MV_STRING8</b>)</p></td>
<td><p>Cadena que contiene valores separados por comas</p></td>
<td><p>Matriz unidimensional que contiene un elemento por cada palabra clave</p></td>
</tr>
</tbody>
</table>


En el siguiente ejemplo de código se muestra cómo agregar una propiedad MAPI de espacio de nombres de cadena al objeto **Table** y cómo afectan las propiedades multivalor a los valore devueltos en un objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)). El procedimiento TableMultiValuedProperties filtra el objeto **Table** por las columnas en las que la propiedad [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) no es una referencia nula. La propiedad **Categories** se representa por una propiedad que usa el espacio de nombres de cadena MAPI. Se crea un filtro de búsqueda y ubicación DAV (DASL) para los elementos que tienen categorías (el filtro actual devuelve las categorías que no tienen una referencia nula). Después se agrega una columna **Categories** al objeto **Table** concatenando el especificador de tipo 0000001f, con la constante categoriesProperty. Por último, el objeto **Column** que representa la propiedad **Categories** contiene una matriz de cadena unidimensional donde cada elemento de la matriz representa una categoría asignada al elemento. Las propiedades **Categories** y **Subject** del elemento se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "http://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

