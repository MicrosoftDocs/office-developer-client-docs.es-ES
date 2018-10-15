---
title: Enviar un elemento de correo con una cuenta de Hotmail
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f95d5202f17c21e1c4be4545687f2eee96a00da3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407306"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a>Enviar un elemento de correo con una cuenta de Hotmail

En este ejemplo se usa la propiedad [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) para enviar un elemento de correo mediante una cuenta de Windows Live Hotmail.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Un perfil define una o más cuentas de correo electrónico, y cada cuenta de correo electrónico está asociada a un servidor de un tipo específico, como Microsoft Exchange Server o el Protocolo de oficina de correo 3 (POP3). Dado que puede tener varias cuentas en el perfil, debe especificar la cuenta de correo electrónico que quiere usar para enviar el elemento y, a continuación, obtener un objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para representarla.

En el siguiente ejemplo de código, se crea un mensaje con un itinerario adjunto y, luego, se envía mediante una cuenta de Windows Live Hotmail. La cuenta de correo electrónico de Hotmail se usa como el objeto **Account** en el perfil de usuario. Después, el ejemplo de código establece la propiedad SendUsingAccount para esa cuenta y llama al método [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) desde el objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Cuentas](accounts.md)

