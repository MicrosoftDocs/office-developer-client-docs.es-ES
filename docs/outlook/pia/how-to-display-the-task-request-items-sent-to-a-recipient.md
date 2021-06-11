---
title: Mostrar los elementos de solicitud de tarea enviados a un destinatario
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9ab5e830003fbfb64b44fc9e0d813c7a7c5163bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357424"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a><span data-ttu-id="a3243-102">Mostrar los elementos de solicitud de tarea enviados a un destinatario</span><span class="sxs-lookup"><span data-stu-id="a3243-102">Display the task request items sent to a recipient</span></span>

<span data-ttu-id="a3243-103">En este ejemplo se explica cómo mostrar todos los elementos de la solicitud de tarea de la Bandeja de entrada del destinatario.</span><span class="sxs-lookup"><span data-stu-id="a3243-103">This example shows how to display all of the task request items that are in a recipient's Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="a3243-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3243-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a3243-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="a3243-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a3243-106">Un objeto [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) representa una solicitud para asignar una tarea a otro usuario.</span><span class="sxs-lookup"><span data-stu-id="a3243-106">A [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) object represents a request to assign a task to another user.</span></span> <span data-ttu-id="a3243-107">El **TaskRequestItem** se crea cuando el elemento se recibe en la Bandeja de entrada del destinatario.</span><span class="sxs-lookup"><span data-stu-id="a3243-107">The **TaskRequestItem** is created when the item is received in the recipient's Inbox.</span></span> <span data-ttu-id="a3243-108">En el siguiente ejemplo de código, ShowTaskRequests filtra la Bandeja de entrada del destinatario, crea un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) y se inserta una fila para cada elemento para el que el valor de la propiedad [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) es igual a **IPM. TaskRequest**.</span><span class="sxs-lookup"><span data-stu-id="a3243-108">In the following code example, ShowTaskRequests filters through a recipient’s Inbox, creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and inserts a row for each item for which the value of the [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) property equals **IPM.TaskRequest**.</span></span> <span data-ttu-id="a3243-109">El asunto de cada tarea en la carpeta de la Bandeja de entrada del destinatario se escribe para los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3243-109">The subject of each task in the recipient’s Inbox folder is then written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="a3243-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a3243-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a3243-111">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="a3243-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a3243-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="a3243-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowTaskRequests()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).GetTable
        (filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a3243-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3243-113">See also</span></span>

- [<span data-ttu-id="a3243-114">Tareas</span><span class="sxs-lookup"><span data-stu-id="a3243-114">Tasks</span></span>](tasks.md)

