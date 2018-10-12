---
title: Filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: bb1abdeb97e15225e77f9e04a4c34e91e70a533a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407460"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="526ff-102">Filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="526ff-102">Filter and display multivalued properties when enumerating items in a folder</span></span>

<span data-ttu-id="526ff-103">En este ejemplo se muestra cómo filtrar y mostrar propiedades multivalor al enumerar elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="526ff-103">This example shows how to filter and display multivalued properties while enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="526ff-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="526ff-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="526ff-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="526ff-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="526ff-106">El objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa un conjunto de datos de elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) o [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="526ff-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="526ff-107">Cuando se agrega por primera vez una propiedad binaria, de fecha o multivalor a un objeto **Table**, la manera en la que se hace referencia a la propiedad afecta a su tipo y a su formato.</span><span class="sxs-lookup"><span data-stu-id="526ff-107">When a binary, date, or multivalued property is first added to a **Table** object, the way the property is referenced affects its type and format.</span></span> <span data-ttu-id="526ff-108">Como las referencias de nombres integrados devuelven a veces un valor de otra columna en lugar de una referencia de espacio de nombres, debe determinar si se hace referencia a la propiedad por su nombre explícito integrado (si procede) o por espacio de nombres (independientemente de la existencia de un nombre explícito integrado).</span><span class="sxs-lookup"><span data-stu-id="526ff-108">Because built-in name references sometimes return a different column value than a namespace reference, you should determine whether the property is referenced by its explicit built-in name (if it has one), or by namespace (regardless of the existence of an explicit built-in name).</span></span> <span data-ttu-id="526ff-109">En la tabla siguiente se muestran las diferencias entre las representaciones de los valores de las propiedades (según su tipo y formato) de acuerdo con el tipo original de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="526ff-109">The following table summarizes the difference in the property value representation (in terms of type and format) per original property type:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="526ff-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="526ff-110">Type</span></span></p></th>
<th><p><span data-ttu-id="526ff-111">Tipo devuelto si la propiedad especificada usa un nombre integrado</span><span class="sxs-lookup"><span data-stu-id="526ff-111">Return type if the specified property uses a built-in name</span></span></p></th>
<th><p><span data-ttu-id="526ff-112">Tipo devuelto si la propiedad especificada usa un espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="526ff-112">Return type if the specified property uses a namespace</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="526ff-113">Binario (<b>PT_BINARY</b>)</span><span class="sxs-lookup"><span data-stu-id="526ff-113">Binary (<b>PT_BINARY</b>)</span></span></p></td>
<td><p><span data-ttu-id="526ff-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="526ff-114">String</span></span></p></td>
<td><p><span data-ttu-id="526ff-115">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="526ff-115">Byte array</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="526ff-116">Fecha (<b>PT_SYSTIME</b>)</span><span class="sxs-lookup"><span data-stu-id="526ff-116">Date (<b>PT_SYSTIME</b>)</span></span></p></td>
<td><p><span data-ttu-id="526ff-117"><b>DateTime</b> local</span><span class="sxs-lookup"><span data-stu-id="526ff-117">Local <b>DateTime</b></span></span></p></td>
<td><p><span data-ttu-id="526ff-118"><b>DateTime</b> UTC</span><span class="sxs-lookup"><span data-stu-id="526ff-118">UTC <b>DateTime</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="526ff-119">Multivalor (también conocido como tipo de palabra clave), como la propiedad <b>Categories</b> (<b>PT_MV_STRING8</b>)</span><span class="sxs-lookup"><span data-stu-id="526ff-119">Multivalued (also known as keyword type) such as <b>Categories</b> property (<b>PT_MV_STRING8</b>)</span></span></p></td>
<td><p><span data-ttu-id="526ff-120">Cadena que contiene valores separados por comas</span><span class="sxs-lookup"><span data-stu-id="526ff-120">String that contains comma-separated values</span></span></p></td>
<td><p><span data-ttu-id="526ff-121">Matriz unidimensional que contiene un elemento por cada palabra clave</span><span class="sxs-lookup"><span data-stu-id="526ff-121">One-dimensional array that contains one element for each keyword</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="526ff-122">En el siguiente ejemplo de código se muestra cómo agregar una propiedad MAPI de espacio de nombres de cadena al objeto **Table** y cómo afectan las propiedades multivalor a los valore devueltos en un objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="526ff-122">The following code example illustrates how to add a MAPI string namespace property to the **Table** object and how multivalued properties affect the values returned in a [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object.</span></span> <span data-ttu-id="526ff-123">El procedimiento TableMultiValuedProperties filtra el objeto **Table** por las columnas en las que la propiedad [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) no es una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="526ff-123">The TableMultiValuedProperties procedure filters the **Table** object for rows where the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) property is not a null reference.</span></span> <span data-ttu-id="526ff-124">La propiedad **Categories** se representa por una propiedad que usa el espacio de nombres de cadena MAPI.</span><span class="sxs-lookup"><span data-stu-id="526ff-124">The **Categories** property is represented by a property that uses the MAPI string namespace.</span></span> <span data-ttu-id="526ff-125">Se crea un filtro de búsqueda y ubicación DAV (DASL) para los elementos que tienen categorías (el filtro actual devuelve las categorías que no tienen una referencia nula).</span><span class="sxs-lookup"><span data-stu-id="526ff-125">A DAV Searching and Locating (DASL) filter is constructed for items that have categories (the actual filter returns categories that do not have a null reference).</span></span> <span data-ttu-id="526ff-126">Después se agrega una columna **Categories** al objeto **Table** concatenando el especificador de tipo 0000001f, con la constante categoriesProperty.</span><span class="sxs-lookup"><span data-stu-id="526ff-126">A **Categories** column is then added to the **Table** object by concatenating the type specifier, 0000001f, with the categoriesProperty constant.</span></span> <span data-ttu-id="526ff-127">Por último, el objeto **Column** que representa la propiedad **Categories** contiene una matriz de cadena unidimensional donde cada elemento de la matriz representa una categoría asignada al elemento.</span><span class="sxs-lookup"><span data-stu-id="526ff-127">Finally, the **Column** object that represents the **Categories** property contains a one-dimensional string array where each element of the array represents a category assigned to the item.</span></span> <span data-ttu-id="526ff-128">Las propiedades **Categories** y **Subject** del elemento se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="526ff-128">Both the item’s **Categories** and **Subject** properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="526ff-129">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="526ff-129">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="526ff-130">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="526ff-130">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="526ff-131">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="526ff-131">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "https://schemas.microsoft.com/mapi/string/"
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

## <a name="see-also"></a><span data-ttu-id="526ff-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="526ff-132">See also</span></span>

- [<span data-ttu-id="526ff-133">Buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="526ff-133">Search and Filter</span></span>](search-and-filter.md)

