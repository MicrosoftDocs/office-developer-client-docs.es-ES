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
# <a name="enumerate-folders"></a><span data-ttu-id="759ab-102">Enumerar carpetas</span><span class="sxs-lookup"><span data-stu-id="759ab-102">Enumerate folders</span></span>

<span data-ttu-id="759ab-103">Este ejemplo muestra cómo enumerar las carpetas mediante iteración por un conjunto de carpetas.</span><span class="sxs-lookup"><span data-stu-id="759ab-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="759ab-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="759ab-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="759ab-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="759ab-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="759ab-106">En el siguiente ejemplo de código, el método EnumerateFoldersInDefaultStore obtiene primero la carpeta raíz del almacenamiento predeterminado mediante el método [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="759ab-106">In the following code example, the EnumerateFoldersInDefaultStore method first obtains the root folder for the default store by using the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) method.</span></span> <span data-ttu-id="759ab-107">Después llama al método EnumerateFolders en la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="759ab-107">It then calls the EnumerateFolders method on the root folder.</span></span> <span data-ttu-id="759ab-108">EnumerateFolders toma una carpeta raíz y recorre las carpetas del almacén predeterminado que representa la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="759ab-108">EnumerateFolders takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="759ab-109">EnumerateFolders primero usa la propiedad [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) para obtener las subcarpetas del objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) raíz.</span><span class="sxs-lookup"><span data-stu-id="759ab-109">EnumerateFolders first uses the [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) property to obtain the subfolders of the root [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="759ab-110">Después se llama de forma recursiva a EnumerateFolders para enumerar todas las carpetas de una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="759ab-110">EnumerateFolders is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="759ab-111">Por último, EnumerateFolders escribe la propiedad [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de cada **Folder** a los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="759ab-111">Finally, EnumerateFolders writes the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property of each **Folder** to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="759ab-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="759ab-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="759ab-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="759ab-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="759ab-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="759ab-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="759ab-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="759ab-115">See also</span></span>

- <span data-ttu-id="759ab-116">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="759ab-116">[Folders](folders.md)</span></span>

