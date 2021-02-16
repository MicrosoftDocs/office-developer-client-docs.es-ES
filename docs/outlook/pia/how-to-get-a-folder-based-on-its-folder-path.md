---
title: Obtener una carpeta con la ruta de acceso
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fed1e7eb39f31ddd4340fc82a16e31ec67523a9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320289"
---
# <a name="get-a-folder-based-on-its-folder-path"></a><span data-ttu-id="bc6f0-102">Obtener una carpeta con la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="bc6f0-102">Get a folder based on its folder path</span></span>

<span data-ttu-id="bc6f0-103">Este ejemplo toma una ruta de acceso y obtiene la carpeta asociada.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-103">This example takes a folder path and obtains the associated folder.</span></span>

## <a name="example"></a><span data-ttu-id="bc6f0-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc6f0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bc6f0-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="bc6f0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="bc6f0-106">En el siguiente ejemplo de código, el método GetKeyContacts usa la propiedad [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) para obtener la ruta de acceso de la carpeta Contactos\\Contactos clave.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-106">In the following code example, the GetKeyContacts method uses the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) property to obtain the folder path of the Contacts\\Key Contacts folder.</span></span> <span data-ttu-id="bc6f0-107">Después se llama al método GetFolder utilizando la propiedad [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) como argumento.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-107">The GetFolder method is then called by using the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property as the argument.</span></span> <span data-ttu-id="bc6f0-108">Si GetFolder devuelve una carpeta, aparecerá un mensaje que indica que se encontraron los contactos clave.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-108">If GetFolder returns a folder, a message will appear saying the Key Contacts are found.</span></span> <span data-ttu-id="bc6f0-109">El método GetFolder toma una ruta de acceso a una carpeta y devuelve el objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) correcto.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-109">The GetFolder method takes in a path to a folder and returns the correct [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="bc6f0-110">Esto se realiza dividiendo primero la propiedad **FolderPath** en una matriz de cadenas y después usando dicha matriz para buscar el objeto **Folder** correcto empezando desde la parte superior de la propiedad **FolderPath**.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-110">This is done by first splitting the **FolderPath** property into a string array and then using the array to find the correct **Folder** object starting from the top of the **FolderPath** property.</span></span> <span data-ttu-id="bc6f0-111">Si no se encuentra la carpeta especificada, GetFolder devuelve una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-111">If the specified folder is not found, GetFolder returns a null reference.</span></span>

<span data-ttu-id="bc6f0-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bc6f0-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bc6f0-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a><span data-ttu-id="bc6f0-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc6f0-115">See also</span></span>

- <span data-ttu-id="bc6f0-116">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="bc6f0-116">[Folders](folders.md)</span></span>

