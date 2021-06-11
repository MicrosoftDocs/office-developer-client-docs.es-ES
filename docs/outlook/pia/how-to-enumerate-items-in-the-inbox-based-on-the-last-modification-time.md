---
title: Enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320359"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a><span data-ttu-id="e1bd1-102">Enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación</span><span class="sxs-lookup"><span data-stu-id="e1bd1-102">Enumerate items in the Inbox based on the last modification time</span></span>

<span data-ttu-id="e1bd1-103">En este ejemplo se muestra cómo enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-103">This example shows how to enumerate items in the Inbox folder based on the last modification time.</span></span>

## <a name="example"></a><span data-ttu-id="e1bd1-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1bd1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e1bd1-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="e1bd1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e1bd1-106">El objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa un conjunto de elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) o [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e1bd1-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of items from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="e1bd1-107">Para obtener un objeto **Table**, llame al método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) en un objeto **Folder** o **Search**.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-107">To obtain a **Table**, call the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on a **Folder** or **Search** object.</span></span> <span data-ttu-id="e1bd1-108">Todos los elementos del objeto **Table** devuelto contienen únicamente un subconjunto predeterminado de sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-108">Each item in the returned **Table** contains only a default subset of the item’s properties.</span></span> <span data-ttu-id="e1bd1-109">Se puede considerar cada objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) como un elemento de la carpeta, y cada objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) como una propiedad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-109">Each [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object can be regarded as an item in the folder, and each [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object as a property of an item.</span></span> <span data-ttu-id="e1bd1-110">En el objeto **Table** no se admite eliminar, agregar ni modificar filas.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-110">Removing, adding, or changing rows is not supported in the **Table**.</span></span> <span data-ttu-id="e1bd1-111">Para enumerar los elementos de un objeto **Table**, use primero la propiedad [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) para ver si la posición actual está al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-111">To enumerate items in a **Table**, first use the [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) property to see whether your current position is at the end of the table.</span></span> <span data-ttu-id="e1bd1-112">Si **EndOfTable** devuelve **false**, use el método [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) para devolver un objeto **Row**, que contiene un número predeterminado de objetos **Column**.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-112">If **EndOfTable** returns **false**, use the [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) method to return a **Row**, which contains a default number of **Column** objects.</span></span> <span data-ttu-id="e1bd1-113">Continúe recorriendo en iteración directamente el objeto **Table** llamando al método **GetNextRow** hasta que **EndOfTable** devuelva **verdadero**.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-113">You continue iterating in a forward manner through the **Table** by calling **GetNextRow** until **EndOfTable** returns **true**.</span></span>

<span data-ttu-id="e1bd1-114">En el ejemplo de código siguiente, DemoTableForInbox obtiene un objeto **Table** para la carpeta Bandeja de entrada, ordena el objeto **Table** usando la propiedad **LastModificationTime** y el método [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), y recorre en iteración la tabla para escribir el asunto de cada elemento en los agentes de escuchas de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1bd1-114">In the following code example, DemoTableForInbox obtains a **Table** object for the Inbox folder, sorts the **Table** object by using the **LastModificationTime** property and [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) method, and iterates through the table to write the subject of each item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="e1bd1-115">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e1bd1-116">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e1bd1-117">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="e1bd1-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e1bd1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1bd1-118">See also</span></span>

- <span data-ttu-id="e1bd1-119">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="e1bd1-119">[Search and filter](search-and-filter.md)</span></span>

