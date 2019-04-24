---
title: Crear un elemento de correo, adjuntar un informe y enviar el elemento de correo al administrador del usuario
TOCTitle: Create a mail item, attach a report, and send the mail item to the user's manager
ms:assetid: 15c26c3b-5e86-4e28-92c5-7389572521da
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644320(v=office.15)
ms:contentKeyID: 55119866
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 32c40e1fbda3f0f851b52d29c073d95a5d636620
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349563"
---
# <a name="create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-users-manager"></a><span data-ttu-id="5e04b-102">Crear un elemento de correo, adjuntar un informe y enviar el elemento de correo al administrador del usuario</span><span class="sxs-lookup"><span data-stu-id="5e04b-102">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>

<span data-ttu-id="5e04b-103">Este ejemplo crea un elemento de correo que tiene datos adjuntos y se lo envía al administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="5e04b-103">This example creates a mail item that has an attachment, and then sends the mail item to the user's manager.</span></span>

## <a name="example"></a><span data-ttu-id="5e04b-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e04b-104">Example</span></span>

<span data-ttu-id="5e04b-105">Este ejemplo se ejecuta correctamente en una cuenta de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5e04b-105">This example runs correctly only against a Microsoft Exchange Server account.</span></span> <span data-ttu-id="5e04b-106">Debe establecerse una relación de administrador para usuarios en el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e04b-106">A manager relationship for users must be established in the Active Directory directory service.</span></span> <span data-ttu-id="5e04b-107">El ejemplo usa el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) para determinar el administrador del usuario actual llamando al método [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5e04b-107">The example uses the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object to determine the current user's manager by calling the [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method.</span></span>

<span data-ttu-id="5e04b-108">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5e04b-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5e04b-109">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="5e04b-109">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5e04b-110">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="5e04b-110">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SendSalesReport()
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.Subject = "Quarterly Sales Report FY06 Q4"
    Dim currentUser As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If currentUser.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            currentUser.GetExchangeUser().GetExchangeUserManager()
        ' Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress)
        mail.Recipients.ResolveAll()
        mail.Attachments.Add("c:\sales reports\fy06q4.xlsx", _
            Outlook.OlAttachmentType.olByValue)
        mail.Send()
    End If
End Sub
```


```csharp
private void SendSalesReport()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Quarterly Sales Report FY06 Q4";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        // Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress);
        mail.Recipients.ResolveAll();
        mail.Attachments.Add(@"c:\sales reports\fy06q4.xlsx",
            Outlook.OlAttachmentType.olByValue, Type.Missing,
            Type.Missing);
        mail.Send();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5e04b-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e04b-111">See also</span></span>

- [<span data-ttu-id="5e04b-112">Correo</span><span class="sxs-lookup"><span data-stu-id="5e04b-112">Mail</span></span>](mail.md)

