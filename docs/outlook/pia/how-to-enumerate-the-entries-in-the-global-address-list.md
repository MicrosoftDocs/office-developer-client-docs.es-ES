---
title: Enumerar las entradas en la lista global de direcciones
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98256ce539172b69c2ae94d495c4aab12e3b8cc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320366"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a><span data-ttu-id="8bcb7-102">Enumerar las entradas en la lista global de direcciones</span><span class="sxs-lookup"><span data-stu-id="8bcb7-102">Enumerate the entries in the Global Address List</span></span>

<span data-ttu-id="8bcb7-103">Este ejemplo enumera las 100 primeras direcciones de Protocolo simple de transferencia de correo (SMTP) principales en la Lista global de direcciones (GAL).</span><span class="sxs-lookup"><span data-stu-id="8bcb7-103">This example enumerates the first 100 primary Simple Mail Transfer Protocol (SMTP) addresses in the Global Address List (GAL).</span></span>

## <a name="example"></a><span data-ttu-id="8bcb7-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8bcb7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8bcb7-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="8bcb7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="8bcb7-106">En el siguiente ejemplo de código, la dirección SMTP de un objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) se obtiene convirtiéndolo en un objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) o [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) en una llamada a los métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) o [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8bcb7-106">In the following code example, the SMTP address for an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object is obtained by casting it to an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) or [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object in a call to the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) or [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) methods.</span></span> <span data-ttu-id="8bcb7-107">Si el objeto **AddressEntry** representa un usuario de Exchange, EnumerateGAL devuelve un objeto **ExchangeUser** que muestra las propiedades del objeto **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-107">If the **AddressEntry** object represents an Exchange user, EnumerateGAL returns an **ExchangeUser** object that exposes properties of the **AddressEntry** object.</span></span> <span data-ttu-id="8bcb7-108">Use propiedades ExchangeUser como [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) o [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) para exponerlas.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-108">Use ExchangeUser properties such as [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)), or [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) to expose them.</span></span>

<span data-ttu-id="8bcb7-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="8bcb7-110">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8bcb7-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateGAL()
{
    Outlook.AddressList gal =
        Application.Session.GetGlobalAddressList();
    if (gal != null)
    {
        for (int i = 1; 
            i <= Math.Min(100, gal.AddressEntries.Count - 1); i++)
        {
            Outlook.AddressEntry addrEntry =
                gal.AddressEntries[i];
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                Outlook.ExchangeUser exchUser =
                    addrEntry.GetExchangeUser();
                Debug.WriteLine(exchUser.Name + " "
                    + exchUser.PrimarySmtpAddress);
            }
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeDistributionListAddressEntry)
            {
                Outlook.ExchangeDistributionList exchDL =
                    addrEntry.GetExchangeDistributionList();
                Debug.WriteLine(exchDL.Name + " "
                    + exchDL.PrimarySmtpAddress);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8bcb7-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bcb7-112">See also</span></span>

[<span data-ttu-id="8bcb7-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="8bcb7-113">Address book</span></span>](address-book.md)

