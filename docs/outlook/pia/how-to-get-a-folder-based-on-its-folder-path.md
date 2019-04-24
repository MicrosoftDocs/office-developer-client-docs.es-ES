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
# <a name="get-a-folder-based-on-its-folder-path"></a>Obtener una carpeta con la ruta de acceso

Este ejemplo toma una ruta de acceso y obtiene la carpeta asociada.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En el siguiente ejemplo de código, el método GetKeyContacts usa la propiedad [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) para obtener la ruta de acceso de la carpeta Contactos\\Contactos clave. Después se llama al método GetFolder utilizando la propiedad [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) como argumento. Si GetFolder devuelve una carpeta, aparecerá un mensaje que indica que se encontraron los contactos clave. El método GetFolder toma una ruta de acceso a una carpeta y devuelve el objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) correcto. Esto se realiza dividiendo primero la propiedad **FolderPath** en una matriz de cadenas y después usando dicha matriz para buscar el objeto **Folder** correcto empezando desde la parte superior de la propiedad **FolderPath**. Si no se encuentra la carpeta especificada, GetFolder devuelve una referencia nula.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Folders](folders.md) (Carpetas)

