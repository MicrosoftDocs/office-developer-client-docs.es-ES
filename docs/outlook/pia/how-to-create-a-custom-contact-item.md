---
title: Crear un elemento de contacto personalizado
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4261fffef0934e01cbfbcc7068377cc392af178c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716430"
---
# <a name="create-a-custom-contact-item"></a>Crear un elemento de contacto personalizado

En este ejemplo se muestra cómo crear un elemento de contacto personalizado y establecer las propiedades predefinidas y las definidas por el usuario.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Un objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) representa un contacto de la carpeta Contactos y tiene más de 100 propiedades integradas, como, por ejemplo, [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) y [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)). A veces, las propiedades integradas no son suficientes y es necesario agregar propiedades personalizadas, lo que puede hacer mediante la colección [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).

En el ejemplo de código siguiente, CreateCustomItem crea un objeto **ContactItem** personalizado, lo denomina "Shoe Store", y llama al método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para agregarlo a una carpeta denominada "Shoe Store". En primer lugar, CreateCustomItem obtiene la carpeta "Shoe Store" mediante el método [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)). La carpeta "Shoe Store" es una subcarpeta de la carpeta Contactos predeterminada. Después, CreateCustomItem establece las propiedades **FirstName** y **LastName**, y crea una propiedad definida por el usuario ("Shoe Size") mediante la colección **UserProperties**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a>Vea también

- [Contactos](contacts.md)

