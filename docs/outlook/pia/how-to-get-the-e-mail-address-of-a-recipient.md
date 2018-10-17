---
title: Obtener la dirección de correo electrónico de un destinatario
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 15e2450e6ab51ea2b34822443914b0f18f3d7c9a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407523"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="bd572-102">Obtener la dirección de correo electrónico de un destinatario</span><span class="sxs-lookup"><span data-stu-id="bd572-102">Gets the email address type of a recipient.</span></span>

<span data-ttu-id="bd572-103">Este ejemplo muestra cómo obtener la dirección del Protocolo simple de transferencia de correo (SMTP) de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="bd572-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="bd572-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd572-104">Example</span></span>

<span data-ttu-id="bd572-105">En el siguiente ejemplo de código, el método GetSMTPAddressForRecipients toma un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) como argumento de entrada y después muestra la dirección SMTP de cada destinatario del elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="bd572-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="bd572-106">El método recupera primero la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) que representa el conjunto de destinatarios especificado para el elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="bd572-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="bd572-107">Después, para cada [destinatario](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) de esa colección **Recipients**, el método obtiene el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) que se corresponde con el objeto **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="bd572-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="bd572-108">Por último, el método usa la propiedad [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) para obtener el valor de la propiedad MAPI https://schemas.microsoft.com/mapi/proptag/0x39FE001E, que asigna a la propiedad **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) del destinatario.</span><span class="sxs-lookup"><span data-stu-id="bd572-108">Finally, the method uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) property of the recipient.</span></span>

<span data-ttu-id="bd572-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bd572-109">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="bd572-110">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="bd572-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bd572-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="bd572-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bd572-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd572-112">See also</span></span>

- [<span data-ttu-id="bd572-113">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="bd572-113">Recipients</span></span>](recipients.md)

