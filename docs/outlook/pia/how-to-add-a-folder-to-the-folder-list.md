---
title: Agregar una carpeta a la lista de carpetas
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dc8ead207261cfd4835e230981d923211771de7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405528"
---
# <a name="add-a-folder-to-the-folder-list"></a><span data-ttu-id="1d298-102">Agregar una carpeta a la lista de carpetas</span><span class="sxs-lookup"><span data-stu-id="1d298-102">Add a folder to the folder list</span></span>

<span data-ttu-id="1d298-103">Este ejemplo muestra cómo usar el método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para agregar una carpeta a la lista de carpetas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1d298-103">This example shows how to use the M:Microsoft.Office.Interop.Outlook._Folders.Add(System.String,System.Object) method to add a folder to the Outlook folder list.</span></span>

## <a name="example"></a><span data-ttu-id="1d298-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d298-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1d298-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="1d298-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="1d298-106">En el siguiente ejemplo de código, **AddMyNewFolder** llama al método **Add** de la colección [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) para agregar un objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) que representa una carpeta denominada “Mi nueva Carpeta” a la **Bandeja de entrada** en la lista de carpetas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1d298-106">In the following code example, **AddMyNewFolder** calls the **Add** method of the [T:Microsoft.Office.Interop.Outlook.Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) collection to add a [T:Microsoft.Office.Interop.Outlook.Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that represents a folder called “My New Folder” to the **Inbox** in the Outlook folder list. “My New Folder” is then displayed.</span></span> <span data-ttu-id="1d298-107">Después se muestra “Mi nueva carpeta”.</span><span class="sxs-lookup"><span data-stu-id="1d298-107">“My New Folder” is then displayed.</span></span>

<span data-ttu-id="1d298-108">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1d298-108">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="1d298-109">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="1d298-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1d298-110">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="1d298-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1d298-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d298-111">See also</span></span>

- <span data-ttu-id="1d298-112">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="1d298-112">[Folders](folders.md)</span></span>

