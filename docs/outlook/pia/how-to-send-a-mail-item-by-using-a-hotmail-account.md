---
title: Enviar un elemento de correo con una cuenta de Hotmail
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 008f66ff1a43f90e756900c467ba6c086829b769
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331167"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a><span data-ttu-id="a99aa-102">Enviar un elemento de correo con una cuenta de Hotmail</span><span class="sxs-lookup"><span data-stu-id="a99aa-102">Send a mail item by using a Hotmail account</span></span>

<span data-ttu-id="a99aa-103">En este ejemplo se usa la propiedad [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) para enviar un elemento de correo mediante una cuenta de Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="a99aa-103">This example uses the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property to send a mail item by using a Windows Live Hotmail account.</span></span>

## <a name="example"></a><span data-ttu-id="a99aa-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a99aa-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a99aa-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="a99aa-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a99aa-106">Un perfil define una o más cuentas de correo electrónico, y cada cuenta de correo electrónico está asociada a un servidor de un tipo específico, como Microsoft Exchange Server o el Protocolo de oficina de correo 3 (POP3).</span><span class="sxs-lookup"><span data-stu-id="a99aa-106">A profile defines one or more email accounts, and each email account is associated with a server of a specific type, such as Microsoft Exchange Server or Post Office Protocol 3 (POP3).</span></span> <span data-ttu-id="a99aa-107">Dado que puede tener varias cuentas en el perfil, debe especificar la cuenta de correo electrónico que quiere usar para enviar el elemento y, a continuación, obtener un objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para representarla.</span><span class="sxs-lookup"><span data-stu-id="a99aa-107">Because you may have multiple accounts in your profile, you must specify which email account you want to use to send the item, and then obtain an [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to represent it.</span></span>

<span data-ttu-id="a99aa-108">En el siguiente ejemplo de código, se crea un mensaje con un itinerario adjunto y, luego, se envía mediante una cuenta de Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="a99aa-108">In the following code example, a message is created with an attached itinerary and then sent by using a Windows Live Hotmail account.</span></span> <span data-ttu-id="a99aa-109">La cuenta de correo electrónico de Hotmail se usa como el objeto **Account** en el perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="a99aa-109">The Hotmail email account is used as the **Account** object in the user’s profile.</span></span> <span data-ttu-id="a99aa-110">Después, el ejemplo de código establece la propiedad SendUsingAccount para esa cuenta y llama al método [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) desde el objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a99aa-110">The code example then sets the SendUsingAccount property to that Account and calls the [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) method from the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span>

<span data-ttu-id="a99aa-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a99aa-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a99aa-112">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="a99aa-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a99aa-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="a99aa-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="a99aa-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="a99aa-114">See also</span></span>

- [<span data-ttu-id="a99aa-115">Cuentas</span><span class="sxs-lookup"><span data-stu-id="a99aa-115">Accounts</span></span>](accounts.md)

