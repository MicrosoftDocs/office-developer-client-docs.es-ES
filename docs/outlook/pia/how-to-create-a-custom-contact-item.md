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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361057"
---
# <a name="create-a-custom-contact-item"></a><span data-ttu-id="53a6c-102">Crear un elemento de contacto personalizado</span><span class="sxs-lookup"><span data-stu-id="53a6c-102">Create a custom Contact item</span></span>

<span data-ttu-id="53a6c-103">En este ejemplo se muestra cómo crear un elemento de contacto personalizado y establecer las propiedades predefinidas y las definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="53a6c-103">This example shows how to create a custom contact item and set both predefined and user-defined properties.</span></span>

## <a name="example"></a><span data-ttu-id="53a6c-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53a6c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="53a6c-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="53a6c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="53a6c-106">Un objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) representa un contacto de la carpeta Contactos y tiene más de 100 propiedades integradas, como, por ejemplo, [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) y [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="53a6c-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object represents a contact in the Contacts folder, and has more than 100 built-in properties such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) and [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span></span> <span data-ttu-id="53a6c-107">A veces, las propiedades integradas no son suficientes y es necesario agregar propiedades personalizadas, lo que puede hacer mediante la colección [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="53a6c-107">Sometimes, the built-in properties are not sufficient and you need to add custom properties, which you can do by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span>

<span data-ttu-id="53a6c-108">En el ejemplo de código siguiente, CreateCustomItem crea un objeto **ContactItem** personalizado, lo denomina "Shoe Store", y llama al método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para agregarlo a una carpeta denominada "Shoe Store".</span><span class="sxs-lookup"><span data-stu-id="53a6c-108">In the following code example, CreateCustomItem creates a custom **ContactItem** object, names it "Shoe Store", and calls the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add it to a folder named "Shoe Store".</span></span> <span data-ttu-id="53a6c-109">En primer lugar, CreateCustomItem obtiene la carpeta "Shoe Store" mediante el método [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="53a6c-109">CreateCustomItem first gets the "Shoe Store" folder by using the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method.</span></span> <span data-ttu-id="53a6c-110">La carpeta "Shoe Store" es una subcarpeta de la carpeta Contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="53a6c-110">The "Shoe Store" folder is a subfolder of the default Contacts folder.</span></span> <span data-ttu-id="53a6c-111">Después, CreateCustomItem establece las propiedades **FirstName** y **LastName**, y crea una propiedad definida por el usuario ("Shoe Size") mediante la colección **UserProperties**.</span><span class="sxs-lookup"><span data-stu-id="53a6c-111">CreateCustomItem then sets the **FirstName** and **LastName** properties, and creates a user-defined property ("Shoe Size") by using the **UserProperties** collection.</span></span>

<span data-ttu-id="53a6c-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="53a6c-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="53a6c-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="53a6c-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="53a6c-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="53a6c-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="53a6c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a6c-115">See also</span></span>

- <span data-ttu-id="53a6c-116">[Contacts](contacts.md) (Contactos)</span><span class="sxs-lookup"><span data-stu-id="53a6c-116">[Contacts](contacts.md)</span></span>

