---
title: Modificar el diseño de una tarjeta de presentación electrónica
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f85324b31ae865c69e2c40806d9654a0b443f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320184"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a><span data-ttu-id="21f60-102">Modificar el diseño de una tarjeta de presentación electrónica</span><span class="sxs-lookup"><span data-stu-id="21f60-102">Modify the layout of an electronic business card</span></span>

<span data-ttu-id="21f60-103">En este ejemplo se muestra cómo modificar el diseño de una tarjeta de presentación electrónica mediante la propiedad [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) de la interfaz [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="21f60-103">This example shows how to modify the layout of an electronic business card by using the [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) property of the [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) interface.</span></span>

## <a name="example"></a><span data-ttu-id="21f60-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21f60-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="21f60-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="21f60-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="21f60-106">Una tarjeta de presentación electrónica ofrece una vista del contacto que captura información específica de ese contacto.</span><span class="sxs-lookup"><span data-stu-id="21f60-106">An electronic business card provides a contact view that captures specific information from that contact.</span></span> <span data-ttu-id="21f60-107">La interfaz **ContactItem** proporciona miembros específicos relacionados con tarjetas de presentación electrónica.</span><span class="sxs-lookup"><span data-stu-id="21f60-107">The **ContactItem** interface provides specific members that pertain to electronic business cards.</span></span> <span data-ttu-id="21f60-108">Estos miembros son los siguientes: **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) y [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="21f60-108">These members are **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)), and [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span></span>

<span data-ttu-id="21f60-109">En el ejemplo de código siguiente, BusinessCardLayoutExample modifica el diseño de una tarjeta de presentación electrónica obteniendo primero un objeto **ContactItem** especificado.</span><span class="sxs-lookup"><span data-stu-id="21f60-109">In the following code example, BusinessCardLayoutExample modifies the layout of an electronic business card by first obtaining a specified **ContactItem** object.</span></span> <span data-ttu-id="21f60-110">En este caso, el objeto **ContactItem** es un contacto en el que el valor de la propiedad [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) es igual a "Melissa MacBeth".</span><span class="sxs-lookup"><span data-stu-id="21f60-110">In this case, the **ContactItem** is a contact with the value of the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property equal to “Melissa MacBeth”.</span></span> <span data-ttu-id="21f60-111">Después, BusinessCardLayoutExample crea una clase de documento XML [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k)y, a continuación, obtiene el atributo de diseño de esta clase en una cadena mediante el valor **BusinessCardLayoutXML** del objeto **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="21f60-111">Next, BusinessCardLayoutExample creates an XML document class [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k), and then gets the layout attribute of this class in a string by using the **BusinessCardLayoutXML** value for the **ContactItem** object.</span></span> <span data-ttu-id="21f60-112">El diseño de la tarjeta se cambia después de alineación a la izquierda a alineación a la derecha.</span><span class="sxs-lookup"><span data-stu-id="21f60-112">The card layout is then changed from left-aligned to right-aligned.</span></span>

<span data-ttu-id="21f60-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="21f60-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="21f60-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="21f60-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="21f60-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="21f60-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="21f60-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="21f60-116">See also</span></span>

- [<span data-ttu-id="21f60-117">Tarjetas de presentación electrónicas</span><span class="sxs-lookup"><span data-stu-id="21f60-117">Electronic business cards</span></span>](electronic-business-cards.md)

