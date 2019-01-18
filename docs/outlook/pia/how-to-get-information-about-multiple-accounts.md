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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703212"
---
# <a name="get-information-about-multiple-accounts"></a>Obtener información sobre múltiples cuentas

Outlook admite un perfil que contenga una o más cuentas conectadas a un servidor Exchange. En este ejemplo se muestra cómo obtener y mostrar información diversa sobre cada cuenta del perfil actual.

## <a name="example"></a>Ejemplo

El método siguiente, EnumerateAccounts, muestra el nombre de cuenta, el nombre de usuario y la dirección de protocolo simple de transferencia de correo (SMTP) para cada cuenta definida en el perfil actual. Si la cuenta está conectada a un servidor Exchange, EnumerateAccounts muestra el nombre de dicho servidor y la información de la versión. Además, si la cuenta reside en un almacén de entrega, EnumerateAccounts muestra el nombre del almacén de entrega predeterminado para la cuenta.

EnumerateAccounts tiene acceso a la mayoría de esta información desde el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), salvo cuando el objeto **Account** no contiene información sobre el nombre de usuario y la dirección SMTP. En ese caso, EnumerateAccounts usa los objetos [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) y [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). 

EnumerateAccounts obtiene el objeto **AddressEntry** mediante el uso de la propiedad [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) del objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) obtenido de la propiedad [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)). EnumerateAccounts obtiene el objeto **ExchangeUser** mediante el uso del método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) del objeto **AddressEntry**. 

A continuación, se muestra el algoritmo para obtener diferente información mediante los objetos Account, AddressEntry y ExchangeUser:

- Si el objeto **Account** contiene información sobre el nombre de usuario y la dirección SMTP, use el objeto **Account** para mostrar el nombre de la cuenta, el nombre de usuario, la dirección SMTP y el nombre del servidor Exchange y la información de la versión si la cuenta es una cuenta de Exchange.

- Si el objeto **Account** no contiene información sobre el nombre de usuario y la dirección SMTP, haga lo siguiente:
    
  - Si la cuenta no es una cuenta de Exchange, use el objeto **AddressEntry** para mostrar el nombre de usuario y la dirección SMTP.
    
  - Si la cuenta es una cuenta de Exchange, haga lo siguiente:
        
    1.  Use el objeto **Account** para mostrar el nombre de cuenta, el nombre del servidor Exchange e información de versión de Exchange.
        
    2.  Use el objeto **ExchangeUser** para mostrar el nombre de usuario y la dirección SMTP.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Cuentas](accounts.md)

