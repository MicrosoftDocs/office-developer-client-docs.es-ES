---
title: Obtener la dirección de correo electrónico de un destinatario
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8957cbc92414b0cdac442167a5c9ea025ce318cb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819339"
---
# <a name="get-the-email-address-of-a-recipient"></a>Obtener la dirección de correo electrónico de un destinatario

Este ejemplo muestra cómo obtener la dirección del Protocolo simple de transferencia de correo (SMTP) de un destinatario.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo de código, el método GetSMTPAddressForRecipients toma un objeto [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) como argumento de entrada y después muestra la dirección SMTP de cada destinatario del elemento de correo. El método recupera primero la colección [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) que representa el conjunto de destinatarios especificado para el elemento de correo. Para cada [Recipient](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) de esa **colección Recipients,** el método obtiene el [objeto PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) que corresponde a ese **objeto Recipient.** Por último, el método usa la [propiedad PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) para obtener el valor de la propiedad MAPI , que se asigna a la propiedad https://schemas.microsoft.com/mapi/proptag/0x39FE001E PR SMTP **\_ \_ ADDRESS**   ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) del destinatario.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a>Vea también

- [Destinatarios](recipients.md)

