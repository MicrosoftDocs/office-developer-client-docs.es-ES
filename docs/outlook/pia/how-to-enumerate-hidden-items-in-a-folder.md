---
title: Enumerar elementos ocultos de una carpeta
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b048ec7fb47a8cbf6b8b49115c59079754fd4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406025"
---
# <a name="enumerate-hidden-items-in-a-folder"></a>Enumerar elementos ocultos de una carpeta

Este ejemplo muestra cómo buscar y enumerar los elementos ocultos en una carpeta.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Una característica del objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), que representa un conjunto de elementos en una carpeta, es que puede contener elementos ocultos. Para devolver los elementos ocultos en una carpeta, establezca el parámetro *TableContents* en el método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) del objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) a [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)). En el siguiente ejemplo de código, TableForInboxHiddenItems obtiene los elementos ocultos de una carpeta Bandeja de entrada y escribe los valores de las propiedades [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) y [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) de cada elemento oculto a los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

-[Buscar y filtrar](search-and-filter.md)

