---
title: Usar matrices para enumerar de forma eficaz elementos de una carpeta
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d165b27da58a4e99eabb897aac3d2dc03811f588
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407509"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a>Usar matrices para enumerar de forma eficaz elementos de una carpeta

Este ejemplo muestra cómo enumerar de forma eficaz los elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) mediante el método [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En el siguiente ejemplo de código, DemoGetArrayForTable obtiene un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) de un objeto **Folder** utilizando el método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)). Después, DemoGetArrayForTable usa el método **GetArray** para devolver un objeto [Array](https://msdn.microsoft.com/library/system.array.aspx) que contiene los elementos de todas las filas de la tabla. El objeto **Array** devuelto es una matriz bidimensional que representa un conjunto de valores de fila y columna de la **tabla**. La matriz está basada en cero, en lugar de en uno, como sucede con las colecciones de Outlook. Una vez que se obtiene el objeto **Array**, el código utiliza un bucle para enumerar por la tabla.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

