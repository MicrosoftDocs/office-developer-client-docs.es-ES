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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338041"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a>Usar SetColumns para enumerar de forma eficaz elementos de una carpeta

En este ejemplo se muestra cómo mejorar el rendimiento de la enumeración de la colección [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) mediante el método [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) para guardar en la memoria caché determinadas propiedades de cada elemento de la colección.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Para enumerar los elementos de una colección, use el método **SetColumns** para guardar en la memoria caché las propiedades de la colección **Items**. **SetColumns** toma un argumento que es una cadena delimitada por comas que representa los nombres de las propiedades. Una vez que se han enumerado todos los elementos de la colección, llame al método [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) para borrar la caché de propiedades.

En el ejemplo de código siguiente, EnumerateContactsWithSetColumns usa el método **SetColumns** para guardar en la memoria caché las propiedades [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) y [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) de los elementos de la carpeta Contactos. Tenga en cuenta que debe comprobar si hay cadenas vacías o una referencia nula en la restricción.

Tenga en cuenta que una carpeta de Outlook puede contener elementos de diferentes tipos. Este ejemplo de código utiliza la clase auxiliar OutlookItem, definida en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para llamar a la propiedad OutlookItem.Class para comprobar la clase de mensaje de cada elemento del subconjunto filtrado de elementos de la carpeta, antes de asumir que el elemento es un elemento de contacto.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

