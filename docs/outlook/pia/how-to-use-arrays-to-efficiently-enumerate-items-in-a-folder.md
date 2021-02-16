---
title: Usar matrices para enumerar de forma eficaz elementos de una carpeta
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be65e2818f22e6da289ef8b8da483c2747f941a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335388"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="d64bd-102">Usar matrices para enumerar de forma eficaz elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="d64bd-102">Use arrays to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="d64bd-103">Este ejemplo muestra cómo enumerar de forma eficaz los elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) mediante el método [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d64bd-103">This example shows how to efficiently enumerate items in a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object by using the [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="d64bd-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d64bd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d64bd-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="d64bd-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d64bd-106">En el siguiente ejemplo de código, DemoGetArrayForTable obtiene un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) de un objeto **Folder** utilizando el método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d64bd-106">In the following code example, DemoGetArrayForTable gets a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from a **Folder** object by using the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method.</span></span> <span data-ttu-id="d64bd-107">Después, DemoGetArrayForTable usa el método **GetArray** para devolver un objeto [Array](https://msdn.microsoft.com/library/system.array.aspx) que contiene los elementos de todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d64bd-107">DemoGetArrayForTable then uses the **GetArray** method to return an [Array](https://msdn.microsoft.com/library/system.array.aspx) object that contains elements for every row in the table.</span></span> <span data-ttu-id="d64bd-108">El objeto **Array** devuelto es una matriz bidimensional que representa un conjunto de valores de fila y columna de la **tabla**.</span><span class="sxs-lookup"><span data-stu-id="d64bd-108">The returned **Array** object is a two-dimensional array that represents a set of row and column values from the **Table**.</span></span> <span data-ttu-id="d64bd-109">La matriz está basada en cero, en lugar de en uno, como sucede con las colecciones de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d64bd-109">The array is zero-based, instead of one-based as is the case with Outlook collections.</span></span> <span data-ttu-id="d64bd-110">Una vez que se obtiene el objeto **Array**, el código utiliza un bucle para enumerar por la tabla.</span><span class="sxs-lookup"><span data-stu-id="d64bd-110">Once the **Array** object is obtained, the code uses a for loop to enumerate through the table.</span></span>

<span data-ttu-id="d64bd-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d64bd-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d64bd-112">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="d64bd-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d64bd-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="d64bd-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d64bd-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="d64bd-114">See also</span></span>

- <span data-ttu-id="d64bd-115">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="d64bd-115">[Search and filter](search-and-filter.md)</span></span>

