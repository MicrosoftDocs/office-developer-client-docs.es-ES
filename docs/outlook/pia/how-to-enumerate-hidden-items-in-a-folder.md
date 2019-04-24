---
title: Enumerar elementos ocultos de una carpeta
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6508ea955ad74b49b5fef73352b4a1706d8e338c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357410"
---
# <a name="enumerate-hidden-items-in-a-folder"></a><span data-ttu-id="cfbff-102">Enumerar elementos ocultos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="cfbff-102">Enumerate hidden items in a folder</span></span>

<span data-ttu-id="cfbff-103">Este ejemplo muestra cómo buscar y enumerar los elementos ocultos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="cfbff-103">This example shows how to find and enumerate hidden items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="cfbff-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cfbff-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="cfbff-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="cfbff-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="cfbff-106">Una característica del objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), que representa un conjunto de elementos en una carpeta, es que puede contener elementos ocultos.</span><span class="sxs-lookup"><span data-stu-id="cfbff-106">One feature of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, which represents a set of items in a folder, is that it may have hidden items.</span></span> <span data-ttu-id="cfbff-107">Para devolver los elementos ocultos en una carpeta, establezca el parámetro *TableContents* en el método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) del objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) a [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="cfbff-107">To return hidden items in a folder, set the *TableContents* parameter in the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object to [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)).</span></span> <span data-ttu-id="cfbff-108">En el siguiente ejemplo de código, TableForInboxHiddenItems obtiene los elementos ocultos de una carpeta Bandeja de entrada y escribe los valores de las propiedades [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) y [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) de cada elemento oculto a los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfbff-108">In the following code example, TableForInboxHiddenItems obtains the hidden items of an Inbox folder, and writes the values of the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) and [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) properties for each hidden item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="cfbff-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="cfbff-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="cfbff-110">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="cfbff-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="cfbff-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="cfbff-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="cfbff-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfbff-112">See also</span></span>

<span data-ttu-id="cfbff-113">-[Buscar y filtrar](search-and-filter.md)</span><span class="sxs-lookup"><span data-stu-id="cfbff-113">-[Search and filter](search-and-filter.md)</span></span>

