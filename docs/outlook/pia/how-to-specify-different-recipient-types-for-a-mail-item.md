---
title: Especificar diferentes tipos de destinatarios de un elemento de correo
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf61a7fbb470291eae448a93c80866112c41407a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335514"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a><span data-ttu-id="c119b-102">Especificar diferentes tipos de destinatarios de un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="c119b-102">Specify different recipient types for a mail item</span></span>

<span data-ttu-id="c119b-103">Este ejemplo muestra cómo establecer mediante programación diferentes tipos de destinatarios (Para, CC o CCO) para un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="c119b-103">This example shows how to programmatically set different recipient types (To, Cc, or Bcc) for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="c119b-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c119b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c119b-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="c119b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="c119b-106">En el siguiente ejemplo de código, se muestra cómo especificar si un destinatario de un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) es un destinatario Para, CC o CCO.</span><span class="sxs-lookup"><span data-stu-id="c119b-106">The following code example illustrates how to specify whether a recipient of a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object is a To, Cc, or Bcc recipient.</span></span> <span data-ttu-id="c119b-107">SetRecipientTypeForMail crea un objeto **MailItem**, agrega tres objetos [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) a la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) de **MailItem** y establece la propiedad [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) para cada objeto **Recipient** a un valor de la enumeración [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c119b-107">SetRecipientTypeForMail creates a **MailItem** object, adds three [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) objects to the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection of the **MailItem**, and then sets the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of each **Recipient** object to a value from the [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) enumeration.</span></span>


> [!NOTE]
> <span data-ttu-id="c119b-108">La propiedad **Type** del objeto **Recipient** es un tipo de entero y no se correlaciona con una enumeración de tipo de destinatarios específica.</span><span class="sxs-lookup"><span data-stu-id="c119b-108">The **Type** property of the **Recipient** object is an int type and does not correlate to a specific recipient type enumeration.</span></span>

<span data-ttu-id="c119b-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c119b-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c119b-110">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="c119b-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c119b-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="c119b-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void SetRecipientTypeForMail()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Sample Message";
    Outlook.Recipient recipTo =
        mail.Recipients.Add("someone@example.com");
    recipTo.Type = (int)Outlook.OlMailRecipientType.olTo;
    Outlook.Recipient recipCc =
        mail.Recipients.Add("someonecc@example.com");
    recipCc.Type = (int)Outlook.OlMailRecipientType.olCC;
    Outlook.Recipient recipBcc =
        mail.Recipients.Add("someonebcc@example.com");
    recipBcc.Type = (int)Outlook.OlMailRecipientType.olBCC;
    mail.Recipients.ResolveAll();
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="c119b-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="c119b-112">See also</span></span>

- [<span data-ttu-id="c119b-113">Correo</span><span class="sxs-lookup"><span data-stu-id="c119b-113">Mail</span></span>](mail.md)

