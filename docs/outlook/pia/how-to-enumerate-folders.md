---
title: Enumerar carpetas
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fe79f78ba1aab1e54df0b0bc88fa0c55c73e187
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710257"
---
# <a name="enumerate-folders"></a>Enumerar carpetas

Este ejemplo muestra cómo enumerar las carpetas mediante iteración por un conjunto de carpetas.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En el siguiente ejemplo de código, el método EnumerateFoldersInDefaultStore obtiene primero la carpeta raíz del almacenamiento predeterminado mediante el método [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)). Después llama al método EnumerateFolders en la carpeta raíz. EnumerateFolders toma una carpeta raíz y recorre las carpetas del almacén predeterminado que representa la carpeta raíz. EnumerateFolders primero usa la propiedad [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) para obtener las subcarpetas del objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) raíz. Después se llama de forma recursiva a EnumerateFolders para enumerar todas las carpetas de una jerarquía. Por último, EnumerateFolders escribe la propiedad [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de cada **Folder** a los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>Vea también

- [Folders](folders.md) (Carpetas)

