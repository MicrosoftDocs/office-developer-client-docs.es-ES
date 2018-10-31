---
title: Obtener una carpeta predeterminada y enumerar sus subcarpetas
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 934b5f823127fde9fbbd3a49f41cedb791277e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407404"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a><span data-ttu-id="bd83d-102">Obtener una carpeta predeterminada y enumerar sus subcarpetas</span><span class="sxs-lookup"><span data-stu-id="bd83d-102">Get a default folder and enumerate its subfolders</span></span>

<span data-ttu-id="bd83d-103">Este ejemplo muestra cómo obtener una carpeta predeterminada del almacén de usuario predeterminado y enumerar sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="bd83d-103">This example shows how to obtain a default folder in the user’s default store and enumerate its subfolders.</span></span>

## <a name="example"></a><span data-ttu-id="bd83d-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd83d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bd83d-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="bd83d-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="bd83d-106">En el siguiente ejemplo de código, GetRSSFeeds usa el método [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para obtener la carpeta raíz de las fuentes RSS del usuario.</span><span class="sxs-lookup"><span data-stu-id="bd83d-106">In the following code example, GetRSSFeeds uses the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to obtain the user’s RSS Feeds root folder.</span></span> <span data-ttu-id="bd83d-107">Después, GetRSSFeeds muestra un cuadro de mensaje que contiene los nombres de carpeta para todas las fuentes RSS en la carpeta Fuentes RSS.</span><span class="sxs-lookup"><span data-stu-id="bd83d-107">GetRSSFeeds then displays a message box that contains the folder names for all RSS feeds in the RSS Feeds folder.</span></span>

<span data-ttu-id="bd83d-108">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bd83d-108">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="bd83d-109">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="bd83d-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bd83d-110">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="bd83d-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetRSSFeeds()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderRssFeeds)
        as Outlook.Folder;
    if (folder != null)
    {
        if (folder.Folders.Count > 0)
        {
            StringBuilder sb = new StringBuilder();
            foreach (Outlook.Folder subfolder
                in folder.Folders)
            {
                sb.AppendLine(subfolder.Name);
            }
            MessageBox.Show(sb.ToString(),
                "RSS Feeds",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bd83d-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd83d-111">See also</span></span>

- <span data-ttu-id="bd83d-112">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="bd83d-112">[Folders](folders.md)</span></span>
