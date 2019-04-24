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
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a>Enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación

En este ejemplo se muestra cómo enumerar los elementos de la carpeta Bandeja de entrada en función de la hora de la última modificación.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

El objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa un conjunto de elementos de un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) o [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Para obtener un objeto **Table**, llame al método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) en un objeto **Folder** o **Search**. Todos los elementos del objeto **Table** devuelto contienen únicamente un subconjunto predeterminado de sus propiedades. Se puede considerar cada objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) como un elemento de la carpeta, y cada objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) como una propiedad de un elemento. En el objeto **Table** no se admite eliminar, agregar ni modificar filas. Para enumerar los elementos de un objeto **Table**, use primero la propiedad [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) para ver si la posición actual está al final de la tabla. Si **EndOfTable** devuelve **false**, use el método [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) para devolver un objeto **Row**, que contiene un número predeterminado de objetos **Column**. Continúe recorriendo en iteración directamente el objeto **Table** llamando al método **GetNextRow** hasta que **EndOfTable** devuelva **verdadero**.

En el ejemplo de código siguiente, DemoTableForInbox obtiene un objeto **Table** para la carpeta Bandeja de entrada, ordena el objeto **Table** usando la propiedad **LastModificationTime** y el método [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), y recorre en iteración la tabla para escribir el asunto de cada elemento en los agentes de escuchas de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

