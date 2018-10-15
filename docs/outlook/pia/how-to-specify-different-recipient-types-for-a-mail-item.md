---
title: Especificar diferentes tipos de destinatarios de un elemento de correo
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9eca70f9c1b77e8430625fb49e3ae9787d337ba7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405535"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a>Especificar diferentes tipos de destinatarios de un elemento de correo

Este ejemplo muestra cómo establecer mediante programación diferentes tipos de destinatarios (Para, CC o CCO) para un elemento de correo.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En el siguiente ejemplo de código, se muestra cómo especificar si un destinatario de un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) es un destinatario Para, CC o CCO. SetRecipientTypeForMail crea un objeto **MailItem**, agrega tres objetos [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) a la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) de **MailItem** y establece la propiedad [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) para cada objeto **Recipient** a un valor de la enumeración [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).


> [!NOTE]
> La propiedad **Type** del objeto **Recipient** es un tipo de entero y no se correlaciona con una enumeración de tipo de destinatarios específica.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Correo](mail.md)

