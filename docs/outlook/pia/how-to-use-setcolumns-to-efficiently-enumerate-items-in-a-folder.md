---
title: Usar SetColumns para enumerar de forma eficaz elementos de una carpeta
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bdfccc6432d35b6f39564e4c87404cc57b6ea27e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708091"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="17eb1-102">Usar SetColumns para enumerar de forma eficaz elementos de una carpeta</span><span class="sxs-lookup"><span data-stu-id="17eb1-102">Use SetColumns to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="17eb1-103">En este ejemplo se muestra cómo mejorar el rendimiento de la enumeración de la colección [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) mediante el método [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) para guardar en la memoria caché determinadas propiedades de cada elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="17eb1-103">This example shows how to improve the performance of enumerating the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection by using the [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) method to cache certain properties of each item in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="17eb1-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17eb1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="17eb1-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="17eb1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="17eb1-106">Para enumerar los elementos de una colección, use el método **SetColumns** para guardar en la memoria caché las propiedades de la colección **Items**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-106">To enumerate items in a collection, use the **SetColumns** method to cache properties on the **Items** collection.</span></span> <span data-ttu-id="17eb1-107">**SetColumns** toma un argumento que es una cadena delimitada por comas que representa los nombres de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="17eb1-107">**SetColumns** takes an argument that is a comma-delimited string that represents property names.</span></span> <span data-ttu-id="17eb1-108">Una vez que se han enumerado todos los elementos de la colección, llame al método [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) para borrar la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="17eb1-108">Once all items in the collection have been enumerated, call the [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) method to clear the property cache.</span></span>

<span data-ttu-id="17eb1-109">En el ejemplo de código siguiente, EnumerateContactsWithSetColumns usa el método **SetColumns** para guardar en la memoria caché las propiedades [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) y [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) de los elementos de la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="17eb1-109">In the following code example, EnumerateContactsWithSetColumns uses the **SetColumns** method to cache the [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) properties of items in the Contacts folder.</span></span> <span data-ttu-id="17eb1-110">Tenga en cuenta que debe comprobar si hay cadenas vacías o una referencia nula en la restricción.</span><span class="sxs-lookup"><span data-stu-id="17eb1-110">Note that you must test for empty strings or a null reference in the restriction.</span></span>

<span data-ttu-id="17eb1-111">Tenga en cuenta que una carpeta de Outlook puede contener elementos de diferentes tipos.</span><span class="sxs-lookup"><span data-stu-id="17eb1-111">Note that an Outlook folder can possibly contain items of different types.</span></span> <span data-ttu-id="17eb1-112">Este ejemplo de código utiliza la clase auxiliar OutlookItem, definida en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para llamar a la propiedad OutlookItem.Class para comprobar la clase de mensaje de cada elemento del subconjunto filtrado de elementos de la carpeta, antes de asumir que el elemento es un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="17eb1-112">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of each item in the filtered subset of items in the folder, before assuming the item is a contact item.</span></span>

<span data-ttu-id="17eb1-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="17eb1-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="17eb1-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="17eb1-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="17eb1-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a><span data-ttu-id="17eb1-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="17eb1-116">See also</span></span>

- [<span data-ttu-id="17eb1-117">Buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="17eb1-117">Search and filter</span></span>](search-and-filter.md)

