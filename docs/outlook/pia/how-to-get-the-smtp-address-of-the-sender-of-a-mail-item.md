---
title: Obtener la dirección SMTP del remitente de un elemento de correo.
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2346257dd2c23f09b77a72b08e17ba51f3f514d1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405556"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a><span data-ttu-id="3629c-102">Obtener la dirección SMTP del remitente de un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="3629c-102">Get the SMTP address of the sender of a mail item</span></span>

<span data-ttu-id="3629c-103">En este ejemplo se obtiene la dirección del protocolo simple de transferencia de correo (SMTP) del remitente de un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="3629c-103">This example gets the sender’s Simple Mail Transfer Protocol (SMTP) address for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="3629c-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3629c-104">Example</span></span>

<span data-ttu-id="3629c-105">Para determinar la dirección SMTP de un elemento de correo recibido, use la propiedad [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) del objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3629c-105">To determine the SMTP address for a received mail item, use the [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="3629c-106">Pero, si el remitente es interno a su organización, **SenderEmailAddress** no devuelve una dirección SMTP y debe usar el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para devolver la dirección SMTP del remitente.</span><span class="sxs-lookup"><span data-stu-id="3629c-106">To determine the SMTP address for a received mail item, use the [P:Microsoft.Office.Interop.Outlook._MailItem.SenderEmailAddress](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) property of the T:Microsoft.Office.Interop.Outlook.MailItem object. However, if the sender is internal to your organization, **SenderEmailAddress** does not return an SMTP address,   and you must use the T:Microsoft.Office.Interop.Outlook.PropertyAccessor object to return the sender’s SMTP address.</span></span>

<span data-ttu-id="3629c-107">En el ejemplo siguiente, GetSenderSMTPAddress usa el objeto **PropertyAccessor** para obtener los valores que no se exponen directamente en el modelo de objetos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="3629c-107">In the following code example, GetSenderSMTPAddress uses the **PropertyAccessor** object to obtain values that are not exposed directly in the Outlook object model.</span></span> <span data-ttu-id="3629c-108">GetSenderSMTPAddress toma un **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="3629c-108">GetSenderSMTPAddress takes in a **MailItem**.</span></span> <span data-ttu-id="3629c-109">Si el valor de la propiedad [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) del **MailItem** recibido es "EX", el remitente del mensaje se encuentra en un servidor Exchange de su organización.</span><span class="sxs-lookup"><span data-stu-id="3629c-109">If the value of the [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) property of the received **MailItem** is "EX", the sender of the message resides on an Exchange server in your organization.</span></span> <span data-ttu-id="3629c-110">GetSenderSMTPAddress usa la propiedad [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) del objeto **MailItem** para obtener el remitente, representado por el objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3629c-110">GetSenderSMTPAddress uses the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem** object to get the sender, represented by the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span> <span data-ttu-id="3629c-111">Si el objeto **AddressEntry** representa un usuario de Exchange, en el ejemplo se llama al método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) para devolver el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) del objeto **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="3629c-111">If the **AddressEntry** object represents an Exchange user, the example calls the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method to return the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object of the **AddressEntry** object.</span></span> <span data-ttu-id="3629c-112">GetSenderSMTPAddress, luego, usa la propiedad [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) del objeto **ExchangeUser** para devolver la dirección SMTP del remitente.</span><span class="sxs-lookup"><span data-stu-id="3629c-112">GetSenderSMTPAddress then uses the [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) property of the **ExchangeUser** object to return the SMTP address of the sender.</span></span> <span data-ttu-id="3629c-113">Si el objeto **AddressEntry** no representa un objeto **ExchangeUser** para el remitente, se usa el método [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) del objeto **PropertyAccessor**, con **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) como argumento, para devolver la dirección SMTP del remitente.</span><span class="sxs-lookup"><span data-stu-id="3629c-113">If the **AddressEntry** object for the sender does not represent an **ExchangeUser** object, the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method of the **PropertyAccessor** object is used, with **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) as the argument, to return the sender’s SMTP address.</span></span>

<span data-ttu-id="3629c-114">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3629c-114">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="3629c-115">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública.</span><span class="sxs-lookup"><span data-stu-id="3629c-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3629c-116">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="3629c-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a><span data-ttu-id="3629c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3629c-117">See also</span></span>

- [<span data-ttu-id="3629c-118">Correo</span><span class="sxs-lookup"><span data-stu-id="3629c-118">Mail</span></span>](mail.md)

