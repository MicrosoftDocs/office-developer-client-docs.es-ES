---
title: Enumerar elementos de una vista de tabla
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3bde66fd07a39aa8a63219876b9bdbcf72e00f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320387"
---
# <a name="enumerate-items-in-a-table-view"></a><span data-ttu-id="0c007-102">Enumerar elementos de una vista de tabla</span><span class="sxs-lookup"><span data-stu-id="0c007-102">Enumerate items in a table view</span></span>

<span data-ttu-id="0c007-103">Este ejemplo enumera los elementos en una vista de tabla utilizando el método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0c007-103">This example enumerates items in a table view by using the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="0c007-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c007-104">Example</span></span>

<span data-ttu-id="0c007-105">El siguiente ejemplo de código obtiene un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) desde la vista actual de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0c007-105">The following code example obtains a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from the current view of the Inbox folder.</span></span> <span data-ttu-id="0c007-106">El ejemplo de código establece la carpeta actual del explorador activo a la Bandeja de entrada y después comprueba que la vista actual de la Bandeja de entrada es una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="0c007-106">The code example sets the current folder of the active explorer to the Inbox, and then checks that the current view of the Inbox is a table view.</span></span> <span data-ttu-id="0c007-107">Si la vista actual es una tabla, el ejemplo de código llama al método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) y muestra cada elemento representado por cada fila en el valor **Table** devuelto.</span><span class="sxs-lookup"><span data-stu-id="0c007-107">If the current view is a table, the code example calls the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method and displays each item represented by each row in the returned **Table**.</span></span>

<span data-ttu-id="0c007-108">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0c007-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0c007-109">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="0c007-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0c007-110">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="0c007-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0c007-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c007-111">See also</span></span>

- [<span data-ttu-id="0c007-112">Vistas</span><span class="sxs-lookup"><span data-stu-id="0c007-112">Views</span></span>](views.md)

