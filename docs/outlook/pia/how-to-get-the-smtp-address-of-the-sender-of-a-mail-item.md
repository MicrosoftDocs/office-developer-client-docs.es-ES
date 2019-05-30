---
title: Obtener la dirección SMTP del remitente de un elemento de correo.
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 05d52f24262f08a6326d464a2dc0d57d6d0510d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542551"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a>Obtener la dirección SMTP del remitente de un elemento de correo.

En este ejemplo se obtiene la dirección del protocolo simple de transferencia de correo (SMTP) del remitente de un elemento de correo.

## <a name="example"></a>Ejemplo

Para determinar la dirección SMTP de un elemento de correo recibido, use la propiedad [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) del objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)). Pero, si el remitente es interno a su organización, **SenderEmailAddress** no devuelve una dirección SMTP y debe usar el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para devolver la dirección SMTP del remitente.

En el ejemplo siguiente, GetSenderSMTPAddress usa el objeto **PropertyAccessor** para obtener los valores que no se exponen directamente en el modelo de objetos de Outlook. GetSenderSMTPAddress toma un **MailItem**. Si el valor de la propiedad [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) del **MailItem** recibido es "EX", el remitente del mensaje se encuentra en un servidor Exchange de su organización. GetSenderSMTPAddress usa la propiedad [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) del objeto **MailItem** para obtener el remitente, representado por el objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)). Si el objeto **AddressEntry** representa un usuario de Exchange, en el ejemplo se llama al método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) para devolver el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) del objeto **AddressEntry**. GetSenderSMTPAddress, luego, usa la propiedad [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) del objeto **ExchangeUser** para devolver la dirección SMTP del remitente. Si el objeto **AddressEntry** no representa un objeto **ExchangeUser** para el remitente, se usa el método [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) del objeto **PropertyAccessor**, con **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) como argumento, para devolver la dirección SMTP del remitente.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    if (mail == null)
    {
        throw new ArgumentNullException();
    }
    if (mail.SenderEmailType == "EX")
    {
        Outlook.AddressEntry sender =
            mail.Sender;
        if (sender != null)
        {
            //Now we have an AddressEntry representing the Sender
            if (sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                //Use the ExchangeUser object PrimarySMTPAddress
                Outlook.ExchangeUser exchUser =
                    sender.GetExchangeUser();
                if (exchUser != null)
                {
                    return exchUser.PrimarySmtpAddress;
                }
                else
                {
                    return null;
                }
            }
            else
            {
                return sender.PropertyAccessor.GetProperty(
                    PR_SMTP_ADDRESS) as string;
            }
        }
        else
        {
            return null;
        }
    }
    else
    {
        return mail.SenderEmailAddress;
    }
}
```

## <a name="see-also"></a>Vea también

- [Correo](mail.md)

