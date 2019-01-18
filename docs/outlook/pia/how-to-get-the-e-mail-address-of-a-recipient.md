---
title: Obtener la dirección de correo electrónico de un destinatario
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 030908f7202301ec7849e655d5ff7cc1d7cffc13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719333"
---
# <a name="get-the-email-address-of-a-recipient"></a>Obtener la dirección de correo electrónico de un destinatario

Este ejemplo muestra cómo obtener la dirección del Protocolo simple de transferencia de correo (SMTP) de un destinatario.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo de código, el método GetSMTPAddressForRecipients toma un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) como argumento de entrada y después muestra la dirección SMTP de cada destinatario del elemento de correo. El método recupera primero la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) que representa el conjunto de destinatarios especificado para el elemento de correo. Después, para cada [destinatario](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) de esa colección **Recipients**, el método obtiene el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) que se corresponde con el objeto **Recipient**. Por último, el método utiliza la propiedad [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) para obtener el valor de la propiedad MAPI https://schemas.microsoft.com/mapi/proptag/0x39FE001E, que se asigna a la **PR\_SMTP\_dirección** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) (propiedad) del destinatario.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Destinatarios](recipients.md)

