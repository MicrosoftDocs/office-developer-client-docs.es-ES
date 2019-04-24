---
title: Obtener información sobre múltiples cuentas
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d065761b9296f1c0eb3043e9b9778e438790f94e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349416"
---
# <a name="get-information-about-multiple-accounts"></a><span data-ttu-id="f4796-102">Obtener información sobre múltiples cuentas</span><span class="sxs-lookup"><span data-stu-id="f4796-102">Get information about multiple accounts</span></span>

<span data-ttu-id="f4796-103">Outlook admite un perfil que contenga una o más cuentas conectadas a un servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4796-103">Outlook supports a profile that contains one or more accounts that are connected to an Exchange Server.</span></span> <span data-ttu-id="f4796-104">En este ejemplo se muestra cómo obtener y mostrar información diversa sobre cada cuenta del perfil actual.</span><span class="sxs-lookup"><span data-stu-id="f4796-104">This example shows how to obtain and display miscellaneous information about each account in the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="f4796-105">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4796-105">Example</span></span>

<span data-ttu-id="f4796-p102">El método siguiente, EnumerateAccounts, muestra el nombre de cuenta, el nombre de usuario y la dirección de protocolo simple de transferencia de correo (SMTP) para cada cuenta definida en el perfil actual. Si la cuenta está conectada a un servidor Exchange, EnumerateAccounts muestra el nombre de dicho servidor y la información de la versión. Además, si la cuenta reside en un almacén de entrega, EnumerateAccounts muestra el nombre del almacén de entrega predeterminado para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f4796-p102">The following method, EnumerateAccounts, displays the account name, user name, and Simple Mail Transfer Protocol (SMTP) address for each account that is defined in the current profile. If the account is connected to an Exchange server, EnumerateAccounts displays the Exchange server name and version information. And if the account resides on a delivery store, EnumerateAccounts displays the name of the default delivery store for the account.</span></span>

<span data-ttu-id="f4796-109">EnumerateAccounts tiene acceso a la mayoría de esta información desde el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), salvo cuando el objeto **Account** no contiene información sobre el nombre de usuario y la dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="f4796-109">EnumerateAccounts accesses most of this information from the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object, except when the **Account** object does not contain information about the user name and SMTP address.</span></span> <span data-ttu-id="f4796-110">En ese caso, EnumerateAccounts usa los objetos [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) y [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f4796-110">In that case, EnumerateAccounts uses the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) and [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) objects.</span></span> 

<span data-ttu-id="f4796-111">EnumerateAccounts obtiene el objeto **AddressEntry** mediante el uso de la propiedad [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) del objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) obtenido de la propiedad [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f4796-111">EnumerateAccounts obtains the **AddressEntry** object by using the [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object obtained from the [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)) property.</span></span> <span data-ttu-id="f4796-112">EnumerateAccounts obtiene el objeto **ExchangeUser** mediante el uso del método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) del objeto **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="f4796-112">EnumerateAccounts obtains the **ExchangeUser** object by using the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method of the **AddressEntry** object.</span></span> 

<span data-ttu-id="f4796-113">A continuación, se muestra el algoritmo para obtener diferente información mediante los objetos Account, AddressEntry y ExchangeUser:</span><span class="sxs-lookup"><span data-stu-id="f4796-113">The following is the algorithm to obtain various information by using the Account, AddressEntry, and ExchangeUser objects:</span></span>

- <span data-ttu-id="f4796-114">Si el objeto **Account** contiene información sobre el nombre de usuario y la dirección SMTP, use el objeto **Account** para mostrar el nombre de la cuenta, el nombre de usuario, la dirección SMTP y el nombre del servidor Exchange y la información de la versión si la cuenta es una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4796-114">If the **Account** object contains information about the user name and SMTP address, use the **Account** object to display the account name, user name, SMTP address, and Exchange server name and version information if the account is an Exchange account.</span></span>

- <span data-ttu-id="f4796-115">Si el objeto **Account** no contiene información sobre el nombre de usuario y la dirección SMTP, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f4796-115">If the **Account** object does not contain information about the user name and SMTP address, proceed as follows:</span></span>
    
  - <span data-ttu-id="f4796-116">Si la cuenta no es una cuenta de Exchange, use el objeto **AddressEntry** para mostrar el nombre de usuario y la dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="f4796-116">If the account is not an Exchange account, use the **AddressEntry** object to display the user name and SMTP address.</span></span>
    
  - <span data-ttu-id="f4796-117">Si la cuenta es una cuenta de Exchange, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f4796-117">If the account is an Exchange account, proceed as follows:</span></span>
        
    1.  <span data-ttu-id="f4796-118">Use el objeto **Account** para mostrar el nombre de cuenta, el nombre del servidor Exchange e información de versión de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4796-118">Use the **Account** object to display the account name, Exchange server name, and Exchange version information.</span></span>
        
    2.  <span data-ttu-id="f4796-119">Use el objeto **ExchangeUser** para mostrar el nombre de usuario y la dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="f4796-119">Use the **ExchangeUser** object to display the user name and SMTP address.</span></span>

<span data-ttu-id="f4796-120">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f4796-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f4796-121">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="f4796-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f4796-122">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="f4796-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAccounts()
{
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        try
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Account: " + account.DisplayName);
            if (string.IsNullOrEmpty(account.SmtpAddress)
                || string.IsNullOrEmpty(account.UserName))
            {
                Outlook.AddressEntry oAE =
                    account.CurrentUser.AddressEntry
                    as Outlook.AddressEntry;
                if (oAE.Type == "EX")
                {
                    Outlook.ExchangeUser oEU =
                        oAE.GetExchangeUser()
                        as Outlook.ExchangeUser;
                    sb.AppendLine("UserName: " +
                        oEU.Name);
                    sb.AppendLine("SMTP: " +
                        oEU.PrimarySmtpAddress);
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
                else
                {
                    sb.AppendLine("UserName: " +
                        oAE.Name);
                    sb.AppendLine("SMTP: " +
                        oAE.Address);
                }
            }
            else
            {
                sb.AppendLine("UserName: " +
                    account.UserName);
                sb.AppendLine("SMTP: " +
                    account.SmtpAddress);
                if(account.AccountType == 
                    Outlook.OlAccountType.olExchange)
                {
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
            }
            if(account.DeliveryStore !=null)
            {
                sb.AppendLine("Delivery Store: " +
                    account.DeliveryStore.DisplayName);
            }
            sb.AppendLine("---------------------------------");
            Debug.Write(sb.ToString());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f4796-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4796-123">See also</span></span>

- [<span data-ttu-id="f4796-124">Cuentas</span><span class="sxs-lookup"><span data-stu-id="f4796-124">Accounts</span></span>](accounts.md)

