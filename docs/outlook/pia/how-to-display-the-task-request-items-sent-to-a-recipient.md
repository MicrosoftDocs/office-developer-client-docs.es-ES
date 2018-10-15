---
title: Mostrar los elementos de solicitud de tarea enviados a un destinatario
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f26e8d1402b75272e79c6244b7bd2875d783c1f1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406641"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>Mostrar los elementos de solicitud de tarea enviados a un destinatario

En este ejemplo se explica cómo mostrar todos los elementos de la solicitud de tarea de la Bandeja de entrada del destinatario.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Un objeto [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) representa una solicitud para asignar una tarea a otro usuario. El **TaskRequestItem** se crea cuando el elemento se recibe en la Bandeja de entrada del destinatario. En el siguiente ejemplo de código, ShowTaskRequests filtra la Bandeja de entrada del destinatario, crea un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) y se inserta una fila para cada elemento para el que el valor de la propiedad [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) es igual a **IPM. TaskRequest**. El asunto de cada tarea en la carpeta de la Bandeja de entrada del destinatario se escribe para los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Tasks](tasks.md) (Tareas)

